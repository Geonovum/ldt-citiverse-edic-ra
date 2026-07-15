# Strategy

<aside class="note">
    This is a first draft for this chapter. It has not been reviewed or can be considered stable as of yet...
</aside>

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

### Descriptive LDT
A Descriptive LDT provides a real-time or near-real-time representation of the current state of an asset or environment. It answers the question: what is happening?

### Diagnostic LDT
A Diagnostic LDT uses operational and sensor data to explain the causes of observed conditions. It provides dashboards with operational insights, answering the question: why is it happening?

### Predictive LDT
A Predictive LDT uses historical and real-time data to forecast future states. It answers the question: what is likely to happen?

### Prospective LDT
A Prospective LDT builds on predictive capabilities and supports the evaluation of potential interventions before they are applied. By executing a prediction model over a modified description of an asset, it enables what-if analysis: what would happen if we acted?

### Prescriptive LDT
A Prescriptive LDT uses real-time data from integrated systems to generate situational awareness and concrete recommendations. It answers the question: what should we do?

### Autonomous LDT
An Autonomous LDT continuously supports or performs decision-making using adaptive and generative AI. It is self-sustaining and continuously learns from new data. It answers the question: what is the right action, and how do I take it?

## LDT Ecosystem

The different types of LDT's can be deployed for different themes within an organisation. This leads to an ecosystem of a common base with shared components with additional capabilities taylored for the specific theme and type of requirements. That is to say, there is not one Digital Twin in an organisation, but a series of connected Local Digital Twins within or even across organisations.

<img src="./respec/media/ldt-ecosystem.png" alt="LDT Ecosystem" width="800">




## Enablement Frameworks

Scaling LDT adoption across cities, regions and communities requires two complementary frameworks realizing the respective enablement capabilities:

- LDT CitiVERSE Technology Framework
Defines the technical components, platform services, integrations and reusable building blocks that implement the LDT capability ecosystem.

- LDT CitiVERSE Enablement Framework
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