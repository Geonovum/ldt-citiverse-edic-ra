
# Motivation and Architectural Guardrails

## Why a European Reference Architecture for Local Digital Twins?

Europe is witnessing rapid growth in the number of Local Digital Twin (LDT) initiatives. Cities, regions and public authorities increasingly use digital twins to support spatial planning, mobility management, climate adaptation, energy transition, infrastructure management and citizen engagement.

While these initiatives share many common goals, they are often developed independently using different technologies, information models, governance arrangements and operational practices. This fragmentation limits the ability to reuse solutions, exchange information, collaborate across borders and create economies of scale.

The LDT CitiVERSE EDIC was established to create a common European framework that enables Local Digital Twins to interoperate and evolve into a networked ecosystem. Rather than promoting a single platform or technology stack, the EDIC aims to establish a shared architectural foundation that allows independently developed solutions to work together, exchange services and build on common assets.

The Reference Architecture therefore serves two complementary purposes:

1. To provide guidance for the development of interoperable Local Digital Twins.
2. To support the creation of shared European infrastructure, services and knowledge that can be reused across Member States.

The architecture recognises that innovation often occurs locally, while interoperability must be achieved globally.

---

## From Digital Twins to a Network of Digital Twins

Traditional digital twins are often designed as standalone solutions tailored to a specific domain or organisation. The LDT CitiVERSE vision moves beyond this approach.

The long-term objective is to create a federated ecosystem of interoperable Local Digital Twins that can:

- Exchange data and services.
- Reuse common capabilities.
- Participate in Data Spaces.
- Share models and algorithms.
- Support European collaboration around common societal challenges.

This vision requires a common architectural approach that balances local autonomy with European interoperability.

The architectural guardrails described in this chapter provide that balance.

---

# Architectural Guardrails

Architectural guardrails are a set of design principles that guide all architecture and implementation decisions within the LDT CitiVERSE ecosystem.

Unlike detailed technical specifications, guardrails provide direction while leaving room for local implementation choices and innovation.

These guardrails should be considered mandatory design objectives for all future reference patterns, building blocks and implementations.

---

## G1 – Interoperability by Design

Interoperability must be considered a primary design objective rather than an afterthought.

Solutions should be designed from the outset to interact with external systems, organisations and communities through open interfaces and agreed standards.

### Rationale

Interoperability is the foundation upon which a network of Local Digital Twins can emerge.

### Implications

- Open APIs are preferred over proprietary interfaces.
- Information exchange should rely on recognised standards.
- Data and services should be discoverable and reusable.
- Components should be usable beyond their original implementation context.
- Although local implementations may opt for less interoperable options, the EDIC will only offer components that comply with this guardrails.

---

## G2 – Federation by Default

The architecture assumes a distributed ecosystem rather than a centralised platform.

Data, services and governance responsibilities should remain as close as possible to their source while still participating in a wider network.

### Rationale

Federation preserves autonomy while enabling collaboration at European scale.

### Implications

- Data remains under local governance wherever possible.
- Services may be distributed across organisations.
- Multiple implementations can coexist.
- Shared infrastructure complements local infrastructure rather than replacing it.

---

## G3 – API First

Capabilities should be exposed through well-defined APIs before user interfaces are considered.

### Rationale

The architecture emphasises service ecosystems rather than monolithic applications.

### Implications

- Services are reusable across multiple applications.
- Automation becomes easier.
- Tool interoperability is improved.
- Integration costs are reduced.

---

## G4 – Reuse Before Build

Before creating a new component, architects and implementers should determine whether an existing capability, service, standard or building block can be reused.

### Rationale

The EDIC exists to create economies of scale and scope through reuse.

### Implications

- Preference for shared services.
- Preference for common building blocks.
- Preference for existing European assets.
- Avoidance of unnecessary duplication.

---

## G5 – Semantic Interoperability First

Systems should exchange meaningful information rather than simply exchanging data.

A shared understanding of concepts, relationships and context is required to support collaboration across domains and countries.

### Rationale

Without semantic interoperability, technical interoperability alone provides limited value.

### Implications

- Use of shared vocabularies.
- Use of semantic technologies where appropriate.
- Explicit metadata.
- Traceable information models.

---

## G6 – Open Standards Before Proprietary Solutions

The architecture promotes the adoption of open and internationally recognised standards.

### Rationale

Open standards reduce barriers to participation and strengthen long-term sustainability.

### Implications

- Preference for standards-based interfaces.
- Preference for open information models.
- Vendor-neutral implementations.
- Easier integration between solutions.

---

## G7 – Data as a Shared Asset

Data should be treated as a strategic asset that can be reused across multiple use cases while respecting governance, privacy and intellectual property constraints.

### Rationale

The value of Local Digital Twins depends on the quality and availability of the data they use.

### Implications

- Data should be discoverable.
- Metadata should be published.
- Provenance should be traceable.
- Data should follow FAIR principles where possible.

---

## G8 – Human-Centred Digital Twins

Technology exists to support people, communities and decision-makers.

The success of a Local Digital Twin should not be measured solely by technical sophistication but by its contribution to better decisions and outcomes.

### Rationale

Digital Twins are tools for people, not ends in themselves.

### Implications

- Focus on user needs.
- Support transparency and explainability.
- Enable participation.
- Promote accessibility and inclusiveness.

---

## G9 – Trust, Privacy and Security by Design

Trust is essential for collaboration across organisations and borders.

Security and privacy considerations must therefore be integrated into every layer of the architecture.

### Rationale

Trust is a prerequisite for sharing data, services and infrastructure.

### Implications

- Secure-by-design implementations.
- Strong identity and access management.
- Data protection compliance.
- Transparent governance arrangements.

---

## G10 – Technology Independence

The architecture should avoid prescribing specific vendors, products or deployment environments.

### Rationale

The architecture should remain relevant despite changing technologies.

### Implications

- Infrastructure portability.
- Cloud neutrality.
- Support for hybrid deployments.
- Support for future technological evolution.

---

