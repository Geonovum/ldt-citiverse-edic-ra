# Application & Technology

## Overview

The Application & Technology layer defines the technical foundation of the LDT CitiVERSE ecosystem.

While the Business & Application layer describes the services that realise Local Digital Twin capabilities, this layer describes the technical platform required to implement, operate and scale those services.

The architecture is based on five fundamental concepts:

- Federated infrastructure
- Shared platform services
- Semantic interoperability
- Orchestration
- Infrastructure-independent deployment

Together these concepts enable Local Digital Twins to be assembled from reusable and interoperable building blocks rather than monolithic applications.

The architecture promotes Local Digital Twins as distributed ecosystems that transform data into knowledge, decisions and interventions through reusable services, common standards and shared infrastructure. This approach allows cities, regions and Member States to collaborate while maintaining local ownership, governance and technical autonomy.

---

# Technical Architecture Principles

The technical architecture implements and operationalises the architectural guardrails introduced earlier in this document.

Specifically, this layer demonstrates how:

- Interoperability by Design is realised through open interfaces.
- Federation by Default is realised through distributed infrastructure.
- Semantic Interoperability is realised through shared information models.
- Reuse Before Build is realised through common platform services.
- Technology Independence is realised through portable deployment models.

The Application & Technology layer defines the infrastructure blueprint for the LDT CitiVERSE ecosystem.

---

# Technology Architecture Stack

The architecture is organised into four logical layers.

```text
Business Services
        ↓
Application Services
        ↓
Technology Services
        ↓
Infrastructure
```

Each layer depends on the services of the layer below while remaining insulated from implementation details.

## Business Services

The business layer provides the stakeholder-facing services described in the previous chapter.

Examples include:

- Digital Participation
- Context Awareness
- Decision Support
- Urban Planning
- Infrastructure Management

## Application Services

Application services realise business services through reusable functionality.

Examples include:

- Data Management
- Visualisation
- Simulation
- Analytics
- Participation
- Identity

## Technology Services

Technology services provide reusable platform capabilities.

Examples include:

- API Management
- Workflow Orchestration
- Context Management
- Event Processing
- Logging
- Monitoring

## Infrastructure

Infrastructure provides the execution environment.

Examples include:

- Cloud Infrastructure
- Edge Infrastructure
- Data Space Infrastructure
- Compute Resources
- Storage Services
- Networking Services

---

# Federated Infrastructure Pattern

## Purpose

The LDT CitiVERSE ecosystem is designed as a federation of independent infrastructures rather than a single central platform.

This allows communities to maintain control over their data, operations and governance while still participating in a broader European ecosystem.

## Architectural Rationale

A federated approach:

- reduces dependency on central infrastructure;
- supports national and local governance requirements;
- enables gradual adoption;
- aligns with Data Space principles;
- supports cross-border collaboration.

## Typical Components

- Data Spaces
- Federated Catalogues
- Shared Registries
- Identity Federations
- Shared Trust Frameworks

## Expected Outcomes

- Cross-community interoperability
- Local autonomy
- European-scale collaboration

---

# Shared Services Architecture

## Purpose

Many Local Digital Twin implementations require similar technical capabilities.

Rather than implementing these capabilities repeatedly, the architecture promotes the reuse of common services.

Shared services provide common capabilities that can be consumed by multiple applications, organisations or Digital Twins.

## Examples

### Data Services

Provide:

- storage
- metadata management
- discovery
- semantic enrichment

### Identity Services

Provide:

- authentication
- authorisation
- trust management

### Knowledge Services

Provide:

- analytics
- reasoning
- AI inference
- simulation

### Observability Services

Provide:

- logging
- monitoring
- auditing
- performance insights

---

# Orchestration Architecture

## Purpose

Orchestration coordinates the interaction between services and building blocks.

Rather than embedding workflow logic within individual applications, orchestration manages the execution sequence between independent components.

## Responsibilities

- Workflow execution
- Service chaining
- Event coordination
- Automation
- Dependency management

## Architectural Significance

Orchestration allows individual building blocks to remain loosely coupled while participating in complex Digital Twin workflows.

This enables both flexibility and interoperability.

### Example

```text
Sensor Data
      ↓
Data Processing
      ↓
Analytics
      ↓
Simulation
      ↓
Visualisation
      ↓
Decision Support
```

Each step may be implemented by an independent service operated by a different organisation.

---

# Semantic Interoperability Architecture

## Purpose

Technical interoperability alone is insufficient for Digital Twin ecosystems.

Systems must also understand the meaning of exchanged information.

The semantic interoperability layer provides this shared understanding.

## Responsibilities

- Semantic alignment
- Context definition
- Metadata management
- Knowledge representation
- Vocabulary management

## Typical Technologies

- RDF
- JSON-LD
- OWL
- Knowledge Graphs
- Ontologies
- DCAT-AP
- SAREF

## Expected Benefits

- Cross-domain integration
- Cross-border interoperability
- Reusable information models
- Improved discoverability

Semantic technologies are a means to shared meaning. They are not, by themselves, a public integration strategy. The next section explains why.

---

# Design-time Contracts, Run-time Queries, and the API Abstraction

Two legitimate ways of working with information meet inside a Local Digital Twin. If they are not separated on purpose, they collapse into one stack — and interoperability suffers.

Call them **design time** and **run time**. They are as distinct as two comic-book universes: each is consistent on its own terms; they do not automatically share a cast. The architecture's job is not to pick a winner. It is to put a common ticket office in front of both.

This section operationalises guardrails G3 (API First), G5 (Semantic Interoperability First), G6 (Open Standards) and G10 (Technology Independence).

## The two worlds

### Design-time schema

At design time, producers and consumers agree the shape of information *before* a question is asked.

Typical artefacts:

- An OpenAPI description of resources, operations and error codes.
- A JSON Schema, XML Schema, or OGC Features schema for a collection.
- A profile that says which properties are mandatory, which vocabularies apply, and which encodings are offered.

Typical public interfaces:

- OGC API — Features, Processes, Records, Tiles
- NGSI-LD as a REST API of context entities
- Ordinary REST resources documented with OpenAPI

The client can be written against a contract. Storage can be anything that can fulfil that contract: files, a relational store, an object store, or a knowledge graph. Transport is HTTP with a documented payload. The client does not need to know how the data is kept.

### Run-time schema

At run time, the shape of the answer is defined *when the question is asked*.

The classic case is SPARQL against RDF. A `SELECT` query invents the columns of the result set. A `CONSTRUCT` query invents the graph that comes back. The schema is a consequence of the query, not a resource that existed beforehand.

This is genuinely powerful. Expert users can ask questions the original publisher did not anticipate. Knowledge graphs can grow without a new API version for every new relationship.

The cost is coupling. In this world, storage format, query language and transport format tend to be the same family of technology. If the public interface is SPARQL, the client must:

- speak SPARQL;
- know the publisher's ontology in enough detail to write a correct query;
- parse RDF (Turtle, JSON-LD, RDF/XML, N-Triples, …);
- accept that the result has no stable resource schema until that particular query is frozen.

The next system that wants to reuse the result is then pressured to stay in RDF as well. That is the **viral aspect** of RDF: not that RDF is closed — it is an open family of standards — but that exposing the store's native language as the public interface forces every participant to adopt that language. Flexibility at the query prompt becomes rigidity in the ecosystem.

The same pattern appears with other native-query interfaces (a vendor's SQL dialect exposed on the internet, a proprietary graph API, a product-specific "data lake query"). RDF is the open and important instance of the pattern in Digital Twin practice; it is not the only one.

## Why practical interoperability is usually higher with a REST API

Flexibility of query and interoperability of systems are not the same quality.

A SPARQL endpoint maximises *what one skilled client can ask*. A documented REST API maximises *how many different clients can participate without sharing a technology stack*.

For a federated network of Local Digital Twins — many organisations, many suppliers, many programming environments, many levels of expertise — the second quality is the scarce one.

A REST API with a design-time contract:

- can be consumed by any HTTP client;
- can be described, tested and procured against OpenAPI or an OGC conformance class;
- can version its resources;
- can offer several encodings of the same resource (GeoJSON, JSON-LD, GML, …);
- can sit in front of RDF, SQL, files or a mix, without advertising that mix to every caller.

A public SPARQL endpoint:

- requires RDF literacy in every client;
- couples callers to the publisher's ontology and to changes in that ontology;
- makes it hard to know, at design time, which properties a downstream process can rely on;
- tends to pull neighbouring systems into the same stack.

This is why the architecture treats **open REST-style APIs as the default public interface** between Local Digital Twins, and treats native query languages (including SPARQL) as powerful capabilities *behind* that interface, or as additional expert interfaces, not as a substitute for it.

Semantic interoperability is not given up. Vocabularies, ontologies and profiles still define meaning. They travel with the API — as JSON-LD contexts, as DCAT metadata, as declared conformance to a profile — rather than requiring every consumer to query a triple store.

NGSI-LD is a useful illustration of the distinction: it carries a linked-data model, but it is offered as a REST API of entities, not as "the client must speak SPARQL".

## The collision

Problems start when the two worlds are treated as one:

- The storage format is used as the transport format.
- The only public schema is the result of a query.
- A city cannot replace the store without replacing every client.
- A second city cannot consume the first city's twin unless it adopts the same graph stack.
- Procurement buys a platform rather than a capability behind a contract.

That is vendor lock-in in slow motion — even when every piece of the stack is open source. Lock-in is dependence on a stack you cannot peel apart, not only dependence on a commercial licence.

## The pattern: an API as abstraction layer

The recommended pattern is an explicit abstraction layer.

```text
  Clients of the twin
  (other twins, apps, tools, Data Spaces)
              │
              │  design-time contract
              │  (REST / OGC API / NGSI-LD / OpenAPI)
              ▼
      ┌───────────────────┐
      │  API abstraction  │  ← public interoperability surface
      └─────────┬─────────┘
                │
     ┌──────────┼──────────────────┐
     ▼          ▼                  ▼
 Design-time   Run-time        Mixed stores
 resources     queries         (files, DB,
 (tables,      (SPARQL,         object store,
  files,        SQL, …)          RDF, …)
  catalogues)
```

Responsibilities of the abstraction layer:

1. **Hide storage.** Clients never attach to the database, file system or triple store.
2. **Publish design-time resources.** Collections, processes, records, tiles and context entities have a documented schema *before* they are called.
3. **Wrap run-time results.** If a SPARQL (or SQL, or other) query is the right way to *produce* an answer, the result is still *published* as a resource with a schema: a feature collection, a process output, a named graph snapshot, a fileset with metadata. The query may be ephemeral; the contract of the published result is not.
4. **Carry meaning.** Metadata, vocabularies and provenance accompany the resource. Meaning is not locked inside a query that only RDF clients can run.
5. **Allow several encodings.** JSON, GeoJSON, JSON-LD, and where needed RDF serialisations, as *options* on the same resource — not as a requirement that every client pick RDF.

### What this means for SPARQL and RDF

RDF, OWL, JSON-LD and SPARQL remain first-class tools for:

- semantic alignment and vocabulary management;
- internal knowledge graphs;
- expert exploration and data science;
- publishing query results *through* the API;
- optional additional endpoints for clients that genuinely need them.

They are not the default handshake of the CitiVERSE federation.

If an implementation exposes SPARQL, it SHOULD also expose the same information (or the operational subset that other twins need) through a design-time REST API. EDIC-offered components MUST do so.

### What this means for REST

REST-style APIs in this architecture are not "JSON instead of semantics". They are the stable surface on which semantics, data and processes are offered to a heterogeneous network.

Where a resource has a well-known meaning, declare it: JSON-LD context, DCAT-AP metadata, a profile URI, a conformance class. That is semantic interoperability without viral coupling of the store.

## Implications for building blocks

| Concern | Design-time (default public surface) | Run-time (behind the API, or expert) |
| --- | --- | --- |
| When is the schema known? | Before the client is written | When the query is issued |
| Typical interface | OGC API, NGSI-LD, OpenAPI | SPARQL, ad-hoc SQL, graph explorers |
| Storage | Hidden | Hidden |
| Transport | HTTP + documented encodings | Native result of the query language |
| Client burden | HTTP + the resource contract | Query language + ontology + parser |
| Risk if used as the *only* public interface | Over-rigid resources, missed questions | Viral stack, weak substitutability |
| Mitigation | Profiles, versioning, optional query APIs | Wrap results as resources; keep SPARQL optional |

Architecture Building Blocks (catalogues, feature access, process execution, context management) are specified at the API-contract level. Solution Building Blocks may use RDF, relational technology, or both. Substitutability is evaluated against the contract, not against the store.

## Expected outcomes

- Cities can change storage technology without rewriting every client.
- A twin that uses a knowledge graph internally can still participate in a REST-based federation.
- A twin that does not use RDF is not excluded from the network.
- Expert SPARQL users keep their power; the rest of the ecosystem is not forced to become SPARQL users.
- Vendor and stack lock-in are reduced because the public dependency is an open API, not a product and not a single technology family.

---

# The Digital Twin Processing Pipeline

A recurring pattern is the transformation of data into knowledge and action.

This pattern realises the LDT Value Stream introduced in the Strategy chapter.

```text
Data Sources
        ↓
Data Integration
        ↓
Semantic Enrichment
        ↓
Processing
        ↓
Analytics & AI
        ↓
Simulation
        ↓
Visualisation
        ↓
Decision Support
        ↓
Intervention
```

The individual stages may be realised by separate services or organisations while collectively forming a coherent Digital Twin ecosystem.

The result is a Digital Twin that acts as a knowledge-generation system rather than merely a data repository.

---

# Infrastructure-Agnostic Deployment

## Purpose

The reference architecture deliberately avoids dependence on specific infrastructure providers.

Solutions should remain portable across different execution environments.

## Supported Deployment Models

- Public Cloud
- Private Cloud
- Sovereign Cloud
- Edge Computing
- Data Space Infrastructure
- National Platforms
- Municipal Platforms
- and all hybrid combinations of the above

## Architectural Benefits

- Technology independence
- Reduced lock-in
- Greater resilience
- Increased portability

---

# Architecture Building Blocks and Solution Building Blocks

The architecture distinguishes between:

## Architecture Building Blocks (ABBs)

Architecture Building Blocks describe reusable architectural capabilities and patterns.

Examples include:

- Data Catalogue
- Simulation Service
- Identity Service
- Semantic Broker

ABBs define *what* capability is required.

## Solution Building Blocks (SBBs)

Solution Building Blocks are concrete implementations of ABBs.

Examples include:

- Products
- Open-source projects
- Cloud services
- Components from the EU LDT Toolbox

SBBs define *how* a capability is implemented.

This distinction enables vendor neutrality while supporting practical implementation. Substitutability is judged against the API contract of the Architecture Building Block, not against the storage format or query language of a particular Solution Building Block. See *Design-time Contracts, Run-time Queries, and the API Abstraction* above.

---

# Shared Infrastructure as a European Commons

At the highest level, the architecture introduces the concept of shared infrastructure as a European commons.

The objective is not to create a single Digital Twin platform, but rather a shared ecosystem of infrastructure, services, standards and knowledge that can be reused across Europe.

Examples include:

- Shared catalogues
- Shared semantic assets
- Shared trust services
- Shared testing facilities
- Shared implementation knowledge

This vision aligns closely with:

- European Data Spaces
- Digital Public Infrastructure initiatives
- EDIC infrastructures
- Cross-border Digital Public Services

---

# From Architecture to Implementation

This layer defines the technical patterns required to implement interoperable Local Digital Twins.

Actual Implementations are out of scope for the reference architecture, but should be following the guardrails and patterns as described in the reference architecture.

```text
Strategy
      ↓
Business & Application
      ↓
Application & Technology
      ↓
Building Blocks
      ↓
      -
Implementations
```

This progression ensures that every technology choice can be traced back to a business objective and ultimately to the strategic goals of the LDT CitiVERSE EDIC.