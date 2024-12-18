# International Data Space Standards (IDSA)

## Background

## Dataspace Protocol Specification

Documentation: https://docs.internationaldataspaces.org/ids-knowledgebase/dataspace-protocol

### Terminology

#### Roles

- Participant: A dataspace member that provides and/or consumes datasets.
- Consumer: A participant agent that requests access to an offered dataset.
- Provider: A participant agent that offers a Dataset.
- Identity provider: A trusted technology system that creates, maintains, and manages identity information for a participant and participant Agents.
- Credential issuer: A trusted technology system that issues verifiable credentials for a participant and participant Agents.
- Participant agent: A technology system that performs operations on behalf of a participant that offers a dataset.
- Dataspace authority: An entity that manages a dataspace. The form and capabilities of a dataspace authority are not covered in these specifications.  

#### Items

- *Agreement*: A (usage) policy agreed between the provider and customers on a specific dataset.
- *Offer*: A concrete policy associate with a specific dataset.
- *Catalog*: A collection of entries representing the datasets and their corresponding offers.
- *Dataset*: Data or a technical service that can be shared by a Participant.
- *DataSpace*: A set of technical services that facilitate interoperable dataset sharing between entities (consumers?).
- *Policy*: A set of rules, duties, and obligations that define the terms of use for a dataset. Also referred to as "Usage Policy".

#### Protocol-related

- Contract Negotiation Protocol: A set of allowable message yype sequences defined as a state machine.
- Transfer Process Protocol: A set of allowable message type sequences defined as a state machine.
- Message: An instantiation of a message type.
- Message Type: A definition of the structure of a Message.

#### Service-related

- Catalog Service: A participant agent that makes a catalog accessible to participants.
- Connector (Data Service): A participant agent that produces agreements and manages dataset sharing.
- Contract Negotiation: A set of instructions between a provider and consumer that establish an agreement. It is an instantiation of the state machine of a contract negotiation protocol.
- Dataspace Registration Service (Dataspace Registry): A technology system that maintains the state of participants in a dataspace. The form and capabilities of a dataspace registration service are not covered in these specifications.
- Transfer Process: A set of interactions between a provider and consumer that give access to a dataset under the terms of an agreement. It is an instantiation of the state machine of a transfer process protocol.

## Available Open-Source Implementations

1. [**DSC** by IDSA][idsa-connector] (since 2020)
2. [**EDC** by Eclipse][eclipse-edc-connector] (since 2021)
3. [**TRUE** by Engineering (an Italy-based digital transformation company)][eng-research-connector] (since 2020)
4. [**Trusted** by Fraunhofer AISEC][aisec-connector] (since 2017)

[idsa-connector]: https://github.com/International-Data-Spaces-Association/DataspaceConnector
[eclipse-edc-connector]: https://github.com/eclipse-edc/Connector
[eng-research-connector]: https://github.com/Engineering-Research-and-Development/true-connector
[aisec-connector]: https://github.com/Fraunhofer-AISEC/trusted-connector

## Resources

### Publications

- [A Survey of Dataspace Connector Implementations. CEUR Workshop. 2023.](https://ceur-ws.org/Vol-3606/paper41.pdf)
  - Describe and compare the four available implementations: [by IDSA][idsa-connector], [by Eclipse][eclipse-edc-connector], [by Engineering][eng-research-connector], [by Fraunhofer AISEC][aisec-connector]


## Certification

(Source: https://internationaldataspaces.org/offers/certification/)

> With the completion of standardization of the **Dataspace Protocol**, the IDS Certification Scheme will evolve to assess interoperability modules based on automated testing.
