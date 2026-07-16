<aside class="note">
    The Archimate models of the <b>reference architecture</b> can be found <a href="https://geonovum.github.io/ldt-citiverse-edic-ra/archimate/" target="_blank_">here.</a>
</aside>

<aside class="note">
    The Archimate models of the EDIC <b>Business architecture</b> can be found <a href="https://geonovum.github.io/ldt-citiverse-edic-ba/archimate/html/index.html" target="_blank_">here.</a>
</aside>

# Introduction

This reference architecture contains guidelines and principles for a networked system of digital twins for the physical environment. This reference architecture is intended for everyone who plays a role in establishing a digital twin for the physical environment. The guidelines, starting points, principles, and standards presented in this document contribute to establishing a system consisting of many applications that form together a network of digital twins.

This document contains an "open" architecture. That is to say: the architecture can be applied by everyone, government and business alike. Application of the guidelines, principles, and standards from this document contributes to establishing an "ecosystem" that consists of many data sources and computational models to be connected. This makes it possible to connect data and models from diverse sectors and knowledge areas, and thereby create two- or three-dimensional images of the physical environment, support policy-making with decision models and simulations, or enable real-time control functionalities for operational processes.

## Why this Architecture Exists

Cities and regions across Europe are increasingly using Local Digital Twins (LDTs) to support urban planning, service delivery, sustainability transitions and public participation. These digital twins combine data, simulation models, analytics and visualisation capabilities to create a shared understanding of the physical and social environment.
Many Local Digital Twin initiatives have emerged independently, often tailored to local needs and implemented using different technologies, data models and governance arrangements. While this diversity stimulates innovation, it also creates challenges for interoperability, reuse and collaboration across cities, regions and Member States.
The LDT CitiVERSE EDIC has been established to address these challenges. Its mission is to create a common European infrastructure that enables Local Digital Twins to exchange information, share services and collaborate across organisational and geographical boundaries. The long-term ambition is to support a network of interoperable Local Digital Twins that together form the foundation of the European CitiVERSE. This Reference Architecture provides a common architectural framework for achieving that ambition.

## Purpose of this Reference Architecture

The purpose of this document is to describe the architectural principles, capabilities, building blocks and interoperability mechanisms required to realise a federated ecosystem of Local Digital Twins.
The architecture does not prescribe a single platform, technology stack or implementation approach. Instead, it defines a set of common patterns and architectural guardrails that enable independent implementations to work together.
Specifically, the Reference Architecture aims to:

- Promote interoperability between Local Digital Twins.
- Support reuse of solutions, building blocks and services.
- Encourage adoption of open standards.
- Provide a common architectural vocabulary.
- Facilitate cross-border collaboration between cities and regions.
- Support the development of shared European infrastructure and services.
- Enable alignment with related European and national initiatives.

The architecture should therefore be understood as a framework for convergence rather than a specification for uniformity.

## Scope

The LDT CiTiVERSE EDIC presents both an architecture of the EDIC itself as well as a reference architecture for LDT CiTiVERSE implementations. This is presented in the following overview picture.

This document is focussed on the Reference architecture for LDT's. The business architecture is documented here: https://geonovum.github.io/ldt-citiverse-edic-ba

<img src="./respec/media/architecture-overview.png" alt="Architecture Overview" width="800">

This document describes the architecture in written form, a more formal definition of the architecture is described using [=Archimate=], which can be found <a href="https://geonovum.github.io/ldt-citiverse-edic-ra/archimate/" target="_blank_">here.</a>

The LDT CitiVERSE EDIC Reference Architecture focuses on the architectural aspects required to create and operate interoperable Local Digital Twins.
The architecture covers:

- Business capabilities and services.
- Application and technology building blocks.
- Data sharing and interoperability mechanisms.
- Semantic interoperability.
- Digital Twin processing and orchestration patterns.
- Shared infrastructure and common services.
- Governance and enablement considerations.

The architecture intentionally spans multiple organisational levels, from individual Local Digital Twin implementations to European-scale infrastructure and collaboration mechanisms.
This document does not prescribe detailed implementation choices, procurement strategies or vendor-specific solutions.

## Intended Audience

This document is intended for a broad audience involved in the development, governance and adoption of Local Digital Twins.
Typical readers include:

- Enterprise architects
- Solution architects
- Digital Twin platform providers
- Data space providers
- Standards organisations
- Policy makers
- Programme managers
- City and regional authorities
- European Digital Infrastructure initiatives

Different chapters can be read independently depending on the interests of the reader. Strategic audiences may focus on the principles, capabilities and governance aspects, while implementation teams may focus on the reference patterns, standards and building blocks.

## Relationship to Other Initiatives

The Reference Architecture does not exist in isolation. It builds on existing work from a variety of European, national and community initiatives.
Particularly relevant are:

- Public report on the LDT Toolbox detailed specifications requirements.
- eGovERA and the European Interoperability Framework.
- European Data Space initiatives.
- Living-in.EU and the Minimal Interoperability Mechanisms (MIMs).
- The EU LDT Toolbox and related Digital Europe projects.
- National and regional Digital Twin initiatives.

The architecture should therefore be seen as part of a broader ecosystem of interoperable digital infrastructure initiatives.

