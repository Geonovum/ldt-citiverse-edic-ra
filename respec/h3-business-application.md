# Business & Application

## Overview

The Business & Application layer describes how Local Digital Twin capabilities are realised through reusable business services, application services and interoperable information flows.

Where the Strategy layer explains **why** Local Digital Twins are needed and **which capabilities** they provide, this layer explains **how those capabilities are implemented** through a combination of reusable services and architectural building blocks.

The architecture promotes a modular and federated approach in which Local Digital Twins are assembled from interoperable components rather than implemented as monolithic solutions. Individual implementations may vary in scope and technology choices, but share a common set of service patterns and interfaces that enable interoperability and reuse across cities, regions and Member States.

The Business & Application layer therefore acts as the bridge between strategic objectives and technology implementation.

---

## Architectural Intent

The primary objective of this layer is to translate LDT capabilities into reusable services that can be shared across multiple implementations.

Three architectural principles drive this layer:

### Interoperability by Design

Services expose capabilities through standard interfaces and information models, allowing independent implementations to collaborate and exchange information.

### Reuse Before Build

Capabilities should be realised using reusable application services and building blocks wherever possible. Solutions should avoid creating bespoke services that duplicate existing functionality.

### Federation by Default

Services may be deployed by different organisations while remaining discoverable and interoperable within a shared ecosystem.

---

# Business Service Architecture

## Business Services as Public Capabilities

Business services provide value directly to communities, public authorities, businesses and citizens.

Rather than focusing on individual software products, the reference architecture focuses on the outcomes these services provide.

A single business service may be realised by multiple application services, and a single application service may contribute to multiple business services.

This separation allows implementations to evolve without changing the business capabilities they support.

---

## Context Awareness

Context Awareness services create a trusted and shared understanding of the current state of an asset, environment or urban system.

### Purpose

Provide operational situational awareness across organisational and domain boundaries.

### Typical Functions

- Sensor integration
- Context aggregation
- Environmental monitoring
- Asset monitoring
- Event detection
- Operational awareness

### Supported LDT Profiles

- Descriptive
- Diagnostic
- Predictive

---

## Co-Creation and Participation

Participation services support collaborative planning and stakeholder engagement.

### Purpose

Enable communities, governments and stakeholders to collectively explore information, evaluate alternatives and support decision-making.

### Typical Functions

- Citizen participation
- Collaborative planning
- Stakeholder engagement
- Feedback collection
- Public consultation
- Scenario evaluation

### Supported LDT Profiles

- Prospective
- Prescriptive

---

## Digital Twin Visualisation

Visualisation services provide a human-centred representation of information, models and simulations.

### Purpose

Transform complex information into understandable insights.

### Typical Functions

- Map visualisation
- 3D city models
- Digital Twin dashboards
- Immersive environments
- Scenario visualisation
- Reporting

### Supported LDT Profiles

- All Profiles

---

## Data Exchange and Collaboration

Data Exchange services support trusted collaboration between organisations.

### Purpose

Enable discovery, sharing and controlled access to information resources.

### Typical Functions

- Data publication
- Data discovery
- Data sharing
- Federated access
- Metadata management
- Data Space participation

### Supported LDT Profiles

- All Profiles

---

## Capability Development and Knowledge Sharing

Capability Development services support organisational maturity and community enablement.

### Purpose

Accelerate LDT adoption and knowledge exchange across communities.

### Typical Functions

- Maturity assessments
- Capability development
- Community support
- Knowledge sharing
- Training
- Best-practice dissemination

---

# Application Service Architecture

Business services are realised through a collection of reusable application services.

Application services are intentionally technology-neutral. Different products may implement the same service as long as they conform to the agreed interfaces and information contracts.

---

## Data Services

### Purpose

Provide the foundation for storing, exchanging and managing information.

### Responsibilities

- Data storage
- Metadata management
- Data cataloguing
- Semantic enrichment
- Data transformation
- Provenance management

### Typical Building Blocks

- Data Catalogues
- Metadata Repositories
- Knowledge Graphs
- Context Brokers
- Data Transformation Services

### Supported Formats

- JSON
- GeoJSON
- JSON-LD
- RDF
- GeoParquet
- NetCDF
- Zarr
- DCAT-AP

---

## Processing Services

### Purpose

Transform information into knowledge.

Processing services sit at the heart of the Generate Knowledge capability and provide analytical and computational functionality.

### Responsibilities

- Data processing
- Analytics
- Machine learning
- Artificial intelligence
- Simulation
- Scenario analysis
- Forecasting

### Typical Building Blocks

- Simulation Engines
- AI Services
- Analytics Services
- Computational Models
- Workflow Engines

---

## Visualisation Services

### Purpose

Provide meaningful and accessible views of information.

### Responsibilities

- Interactive dashboards
- Geospatial visualisation
- 3D environments
- XR visualisation
- Reporting

### Typical Building Blocks

- Dashboard Services
- Map Services
- Digital Twin Viewers
- XR Platforms

---

## Participation Services

### Purpose

Enable interaction between people and digital twin systems.

### Responsibilities

- Consultation
- Stakeholder engagement
- Collaborative planning
- Decision support workshops
- Feedback collection

### Typical Building Blocks

- Participation Platforms
- Collaboration Portals
- Consultation Services

---

## Integration Services

### Purpose

Connect independent systems and services into a coherent ecosystem.

### Responsibilities

- Service federation
- API management
- Identity federation
- Information mediation
- Logging and monitoring

### Typical Building Blocks

- API Gateways
- Identity Providers
- Service Registries
- Federation Services
- Observability Platforms

---

# Service Realisation Pattern

A recurring pattern throughout the architecture is that business services are realised through multiple application services working together.

For example:

```text
Context Awareness
        │
        ├──────── Data Services
        │
        ├──────── Integration Services
        │
        ├──────── Processing Services
        │
        └──────── Visualisation Services
```

Likewise:

```text
Citizen Participation
        │
        ├──────── Participation Services
        │
        ├──────── Visualisation Services
        │
        ├──────── Data Services
        │
        └──────── Identity Services
```

This pattern allows services to be reused across domains while maintaining a consistent user experience.

---

# Open Interfaces and Standards

To enable interoperability, all application services should expose their functionality through open interfaces.

## API Standards

- OGC API Features
- OGC API Processes
- OGC API Records
- OGC API Tiles
- NGSI-LD
- SPARQL

## Trust and Identity

- OpenID Connect
- OIDC Federation
- OID4VC
- Verifiable Credentials

## Observability

- OpenTelemetry
- Structured Logging
- Monitoring Services

## Data Sharing

- Dataspace Protocol
- IDS Catalog Protocol
- Federated Discovery Mechanisms

---

# Information Models and Semantic Assets

Information interoperability depends on the use of shared information models and semantic assets.

The architecture therefore promotes the use of common vocabularies, ontologies and information models that can be reused across Local Digital Twin implementations.

### Examples

- DCAT-AP
- PROV-O
- SAREF
- IFC
- JSON-LD Contexts
- Linked Open Vocabularies
- Verifiable