# Strategy

## Overview

The LDT CitiVERSE reference architecture is organised around a number of __capabilities.__ A Local Digital Twin (LDT) is not a single application. It is a composition of interoperable capabilities that together enable cities and regions to integrate data, generate knowledge, support decisions and act on real-world situations.
The architecture is structured around a central __value stream__ — the LDT / Data Value Stream — which represents the progression from data integration to actionable outcomes. This value stream is supported by both technical and community enablement capabilities.
LDT CitiVERSE capabilities are grounded in the broader eGovERA capability framework, which provides the European public-sector architecture context for Digital Twin, Knowledge Management, Data Management and Artificial Intelligence.

## LDT / Data Value Stream

<img src="./respec/media/ldt-value-stream.png" alt="LDT Value Stream" width="800">

The LDT / Data Value Stream defines how a Local Digital Twin creates value. 

## LDT CitiVERSE Capabilities

The value stream consists of four sequential capability stages:

1. __Digital Foundation / Integration__
The LDT establishes a technical and data foundation that connects data sources, services and components. This stage provides the interoperability layer on which all subsequent capabilities depend.

2. __Generate Knowledge__
Integrated data is transformed into knowledge, insight and intelligence. This stage encompasses analysis, modelling and AI-driven inference that produce actionable information for stakeholders.

3. __Decide__
The LDT supports evidence-based decision-making. Decision makers receive insight and recommendations derived from the knowledge generated in the previous stage.

4. __Intervene__
Decisions are connected to concrete actions or interventions in the physical, organisational or policy environment. This stage closes the loop between digital insight and real-world change.

Furthermore there are two enabling capabilities:

5. __Technical Enablement__
Reusable technical building blocks and platform services

6. __Community Enablement__
Adoption support, knowledge sharing and community building

These capabilities together define what the LDT CitiVERSE ecosystem must provide to cities, regions and their partners.

## Types of Local Digital Twins

Local Digital Twins are categorised by their level of analytical and decision-support maturity. Each type builds on the capabilities of the preceding type. The main premise is that not all implementations need the same type of LDT, depending on the requirements the right type of LDT should be implemented. Also an organisation will likely have multiple LDT's for different projects in different lifecycle stages. While they should be based on the same common core components, the specific type needs to be tailored to the needed requirements.

### Conformance Profiles

Not every Local Digital Twin requires the same capabilities, level of sophistication, or operational complexity.

The LDT CitiVERSE Reference Architecture therefore defines a series of **Conformance Profiles**. These profiles establish a common understanding of the minimum capabilities that an implementation must provide in order to be considered a specific type of Local Digital Twin.

The profiles serve several purposes:

- Provide guidance for communities implementing Local Digital Twins.
- Support procurement and solution selection.
- Enable interoperability testing and validation.
- Support future EDIC certification schemes.
- Provide a roadmap for the gradual evolution of Local Digital Twin implementations.

The profiles are cumulative: each profile builds upon the capabilities of the previous profile.

#### Common Foundation Requirements

All Local Digital Twins participating in the LDT CitiVERSE ecosystem must provide a common foundation that supports interoperability and collaboration.

#### Mandatory Capabilities

- Digital Foundation / Integration
- Technical Enablement
- Community Enablement

#### Mandatory Characteristics

- Standards-based APIs
- Metadata publication and discovery
- Identity and access management
- Open interoperability interfaces
- Conformance to the architectural guardrails
- Participation in federated discovery mechanisms

These requirements represent the minimum baseline for participation in the LDT CitiVERSE ecosystem.

### Profile 1 – Descriptive LDT

#### Purpose

A Descriptive LDT provides a real-time or near-real-time representation of the current state of an asset, area, system or environment.

#### Primary Question

> What is happening?

#### Required Capabilities

| Capability | Requirement |
|------------|------------|
| Digital Foundation / Integration | Required |
| Data Ingestion | Required |
| Visualisation | Required |
| Metadata Management | Required |
| Discovery Services | Required |

#### Typical Building Blocks

- Data Catalogue
- Data Store
- Context Management Services
- Dashboard Services
- Map Viewers
- Sensor Integration Services

#### Typical Outputs

- Operational dashboards
- Current status views
- Situation awareness
- Shared operational picture

---

### Profile 2 – Diagnostic LDT

#### Purpose

A Diagnostic LDT explains observed conditions and identifies underlying causes.

#### Primary Question

> Why is it happening?

#### Additional Required Capabilities

| Capability | Requirement |
|------------|------------|
| Descriptive Profile | Required |
| Knowledge Generation | Required |
| Analytics Services | Required |
| Correlation Analysis | Required |

#### Typical Building Blocks

- Analytics Services
- Monitoring Services
- Data Quality Services
- Event Processing Services
- Knowledge Graph Services

#### Typical Outputs

- Root-cause analysis
- Performance diagnostics
- Explanatory insights
- Operational intelligence

---

### Profile 3 – Predictive LDT

#### Purpose

A Predictive LDT forecasts future conditions using historical and real-time information.

#### Primary Question

> What is likely to happen?

#### Additional Required Capabilities

| Capability | Requirement |
|------------|------------|
| Diagnostic Profile | Required |
| Predictive Analytics | Required |
| Forecasting | Required |
| Simulation | Required |

#### Typical Building Blocks

- Forecasting Services
- Machine Learning Models
- Simulation Engines
- Scenario Data Services

#### Typical Outputs

- Forecasts
- Trend predictions
- Early-warning indicators
- Impact forecasts

---

### Profile 4 – Prospective LDT

#### Purpose

A Prospective LDT evaluates alternative futures by exploring the consequences of potential interventions before they are applied.

#### Primary Question

> What would happen if we acted?

#### Additional Required Capabilities

| Capability | Requirement |
|------------|------------|
| Predictive Profile | Required |
| Scenario Management | Required |
| What-if Analysis | Required |
| Model Composition | Required |

#### Typical Building Blocks

- Computational Models
- Scenario Engines
- Model Orchestration Services
- Intervention Analysis Services

#### Typical Outputs

- Scenario comparisons
- Impact assessments
- Alternative futures
- Policy evaluation

---

### Profile 5 – Prescriptive LDT

#### Purpose

A Prescriptive LDT recommends actions based on data, models and simulated outcomes.

#### Primary Question

> What should we do?

#### Additional Required Capabilities

| Capability | Requirement |
|------------|------------|
| Prospective Profile | Required |
| Decision Support | Required |
| Recommendation Services | Required |
| Optimisation | Required |

#### Typical Building Blocks

- Decision Support Systems
- Optimisation Engines
- Recommendation Services
- Policy Evaluation Services

#### Typical Outputs

- Ranked interventions
- Action recommendations
- Resource optimisation
- Decision support products

---

### Profile 6 – Autonomous LDT

#### Purpose

An Autonomous LDT continuously evaluates situations and can automatically execute or propose interventions within agreed governance constraints.

#### Primary Question

> What is the right action and how can it be implemented?

#### Additional Required Capabilities

| Capability | Requirement |
|------------|------------|
| Prescriptive Profile | Required |
| Autonomous Decision Support | Required |
| Adaptive Learning | Required |
| Automated Orchestration | Required |
| Governance Controls | Required |

#### Typical Building Blocks

- Agent-based AI Services
- Workflow Orchestration
- Adaptive Learning Services
- Policy Enforcement Services
- Human Oversight Services

#### Typical Outputs

- Automated interventions
- Dynamic optimisation
- Self-learning behaviour
- Closed-loop operations

---

## Capability Progression

The six conformance profiles represent an increasing level of maturity and capability.

```text
Observe
   ↓
Understand
   ↓
Predict
   ↓
Explore
   ↓
Recommend
   ↓
Act
```

Mapped to the LDT types:

```text
Descriptive
      ↓
Diagnostic
      ↓
Predictive
      ↓
Prospective
      ↓
Prescriptive
      ↓
Autonomous
```

Importantly, higher maturity levels do not replace lower ones. A mature Local Digital Twin continues to provide descriptive, diagnostic and predictive functionality while adding progressively more advanced analytical and decision-support capabilities. Not all themes or solutions need to evolve to the higher levels.

---

## Selecting an Appropriate Profile

Not every use case requires an Autonomous Local Digital Twin.

For example:

| Use Case | Typical Profile |
|-----------|-----------|
| Shared Operational Picture | Descriptive |
| Infrastructure Monitoring | Diagnostic |
| Flood Forecasting | Predictive |
| Urban Planning Scenarios | Prospective |
| Traffic Optimisation | Prescriptive |
| Dynamic Energy Management | Autonomous |

Communities should select the profile that best matches the objectives, risks, governance requirements and operational context of their implementation.

The Reference Architecture therefore supports a diversity of Local Digital Twins while ensuring that implementations remain interoperable and aligned with a common European architectural framework.

---

## LDT Ecosystem

The different types of LDT's can be deployed for different themes within an organisation. This leads to an ecosystem of a common base with shared components with additional capabilities taylored for the specific theme and type of requirements. That is to say, there is not one Digital Twin in an organisation, but a series of connected Local Digital Twins within or even across organisations.

<img src="./respec/media/ldt-ecosystem.png" alt="LDT Ecosystem" width="800">




## Enablement Frameworks

Scaling LDT adoption across cities, regions and communities requires two complementary frameworks realizing the respective enablement capabilities:

- LDT CitiVERSE __Technology Framework__
Defines the technical components, platform services, integrations and reusable building blocks that implement the LDT capability ecosystem.

- LDT CitiVERSE __Enablement Framework__
Defines the organisational, community and adoption capabilities that support the uptake, operation and governance of Local Digital Twins across participating organisations.

## Artificial Intelligence

Artificial Intelligence is a cross-cutting capability within the LDT CitiVERSE architecture. It contributes primarily to the Generate Knowledge stage of the value stream, through two specialised subcapabilities:

Urban Intelligence & ML Inference — the application of machine learning models to urban data to generate intelligence and predictions

Collaborative Knowledge Training — the shared development and improvement of AI models across communities and organisations

AI is also central to the Autonomous LDT type, where adaptive and generative AI enable continuous, self-sustaining decision support.

<aside class="note">
    As is already stated earlier, this is an evolving reference architecture. Specifically for a topic like AI there are a lot of innovations happening. A seperate activity of the EDIC LDT CiTiVERSE is the establisment of a Technologies Assesment Framework. Through this assesment framework technology components will be evaluated and potentially added to the reference architecture.
</aside>

## Relationship to eGovERA

LDT CitiVERSE capabilities are specialisations of capabilities defined in the eGovERA European Government Enterprise Reference Architecture. The mapping is as follows:

| eGovERA Capability | LDT CitiVERSE Specialisation | 
| --- | --- |
| Digital Twin | LDT types and Data Value Stream |
| Knowledge Management | Generate Knowledge capability |
| Data Management | Digital Foundation / Integration |
| Artificial Intelligence | Urban Intelligence, ML Inference, Collaborative Training |

This alignment ensures that the LDT CitiVERSE architecture is compatible with the broader European public-sector architecture landscape and can be adopted consistently across member states.



