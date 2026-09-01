# Glossary

<dfn>Archimate</dfn> Open and independent modeling language for Enterprise Architecture. See: [Open Group Archimate Overview](https://www.opengroup.org/archimate-forum/archimate-overview)

<dfn>API abstraction layer</dfn> A documented public interface that sits between clients and storage. It hides how data is kept (files, database, RDF, …) and how ad-hoc queries are executed, and offers resources with a schema that is known before the client is written.

<dfn>Design-time schema</dfn> An information contract agreed before a question is asked: OpenAPI, JSON Schema, an OGC Features schema, a profile. Clients can be written against it. Storage and transport are allowed to differ.

<dfn>Run-time schema</dfn> An information shape that exists only as the result of a query, for example a SPARQL `SELECT` or `CONSTRUCT`. Powerful for exploration; a poor default as the only public interface of a federated Digital Twin.

<dfn>Vendor lock-in</dfn> Dependence on a product or a technology stack that cannot be peeled apart. It occurs when storage format, transport format and query language collapse into one interface — including when that stack is open source.