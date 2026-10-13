# Summary

A Local Digital Twin (LDT) is a living digital picture of a city, neighbourhood or region. It combines data, models and views so people can see what is happening, understand why, try "what if" questions, and decide what to do.

Europe already has many of these twins. Most were built separately: different software, different data formats, different ways of talking to other systems. That is fine for a single project. It becomes a problem when cities want to reuse each other's work, connect twins across borders, or switch suppliers without starting over.

This reference architecture is not a product catalogue and not a single European mega-twin. It is a shared set of rules and patterns so independently built twins can still work together.

If you only read one chapter, read this summary.

## Why standards? Interoperability is the point

If every twin speaks a private language, connecting them is expensive and fragile. Standards are the common language.

There are three kinds of "speaking the same language":

1. **Technical** — can the systems actually connect? (HTTP APIs, identity, catalogues.)
2. **Semantic** — do they mean the same thing by "building", "flood", or "energy label"?
3. **Organisational** — who is allowed to share what, under which rules?

Without all three, you get data dumps that nobody can safely reuse.

Open standards — for example OGC APIs, DCAT catalogues, OpenID Connect, and Data Space protocols — do three practical jobs:

- They let a city mix building blocks from different suppliers.
- They let a twin in one place consume a service from another.
- They make procurement and replacement possible, because you buy a capability behind a known interface, not a closed stack.

A Digital Twin that cannot talk to the next Digital Twin is a silo with a 3D view. The network of twins is the actual product.

## Patterns that keep you out of vendor lock-in

Lock-in happens when the way you *store* data, the way you *send* data, and the way you *ask questions* are all tied to one product — or even to one technology family.

These patterns break that knot:

1. **API first, not platform first.** Expose capabilities as well-defined APIs. The user interface is one consumer among many, not the product itself.
2. **Federation, not a central platform.** Data and services stay with their owners. Europe connects them; it does not vacuum them into one cloud.
3. **Separate "what" from "how".** The architecture describes building blocks (a catalogue, a simulation service, an identity service). Many products can implement the same block. You can replace a product without changing the architecture.
4. **Portable deployment.** Run on public cloud, private cloud, edge, or a municipal server. The architecture does not pick a vendor's cloud.
5. **Reuse before you build.** Prefer a shared European or national component over a custom one-off.
6. **Decouple storage from exchange.** How data is stored internally (files, a database, a knowledge graph) must not dictate how partners consume it. Partners talk to an API, not to the store.

## Design time versus run time — two worlds, one ticket office

This last pattern is easy to miss, and expensive when it is missed.

**Design time** is when you agree the shape of information *before* anyone asks a question. A REST API with an OpenAPI description, or an OGC API with a known feature schema, is design-time: clients know the contract in advance. Storage and transport can differ. You can keep data in PostgreSQL and still serve GeoJSON over HTTP.

**Run time** is when the shape of the answer is defined *when you ask the question*. SPARQL against RDF is the classic example: the query creates the schema of the result. That is powerful. It is also tightly coupled. The store, the query language and the payload belong to the same technology family. If the public interface is SPARQL, every client must speak RDF. That tends to spread: once one part of the chain is RDF-only, the rest is pressured to become RDF-only too. That is the viral aspect of RDF — not a moral judgement, a network effect.

Both worlds are useful. They collide when a twin tries to be both a flexible knowledge graph *and* a practical service for many different clients, without an adapter in between. Think of two comic-book universes: each is consistent inside its own rules; they do not share a cast until someone builds a crossover. The crossover is not "make everyone speak RDF" or "forbid SPARQL". The crossover is a ticket office both audiences can use.

The practical way out is an **abstraction layer**: a stable API in front of whatever lives behind it.

- Behind the API, a city may store data as tables, files, or RDF.
- In front of the API, clients get a documented resource: features, processes, records, tiles, context entities.
- If someone needs an ad-hoc SPARQL-style question, the *result* of that query can still be published through the same API, with a schema the next client can rely on.

For a network of twins, **practical interoperability is usually higher with a REST-style API** than with exposing the store's native language. REST does not forbid RDF internally. It forbids making RDF — or any other store format — the only way in.

## What to remember

- Many twins, one network — not one European mega-twin.
- Open APIs and open standards are how twins collaborate without becoming the same product.
- Keep storage, transport and query language from collapsing into one stack, proprietary or not.
- Put an API between how data is kept and how data is used.

The chapters that follow are the detailed architecture: capabilities, services and technology patterns that put these ideas into practice. The expanded argument on design-time versus run-time contracts is in the Application & Technology chapter.
