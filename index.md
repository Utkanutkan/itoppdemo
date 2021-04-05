# Welcome to Traceability Blockchain Prototype

## Introduction

This is the repository for traceability blockchain prototype. This repository includes three compoenents. Tracegui includes the tracegui application, traceapp includes the traceapi and trace conctract, external includes the code to access the traceapi from another client.

The installations were tested on Ubuntu 20.04 LTS with a configuration of 2 GB RAM. 

```markdown

```
## Installation

The prototype uses the Hyperledger Fabric 1.4. The detailed installation instructions is given in Hyperledger Fabric page(https://hyperledger-fabric.readthedocs.io/en/release-1.4/prereqs.html). After installing the fabric you need to run first network and install the standartparts smart contract.

```markdown

```

After installing the fabric you need to start the first network from fabric samples. 
```markdown

```
The standard parts contract should be started afterwards.


## Prototype Architecture, starting traceapi and tracegui
The traceapi is a node.js application. Ideally every organization runs a copy of their api. The blockchain api uses wallet and blockchain network configuration to access the blockchain. In the current configuration organizational wallet is included in the api. The tracegui is a vuetify application and calls the api functions.

The api files are copied to a folder. Node files are built and api server is started.

```markdown

```

The client gui is also coped to folder in the aerver machine. The configuration of the api should be present in the client gui.

```markdown

```
The client web applicaiton is built and started. 

```markdown

```
.Finally check the application from the you browser. The initial three parts that ecist in the initial contract can be seen/

```markdown

```

## The Scenario

The scenario is run on a presinstalled tracegui, traceapp and blockchain. tracegui is cloud hosted and accessed through [itopp.nl/ORGID](itopp.nl/ORG1). The api can be accessed through [partsledger.tk/transactionname](partsledger.tk/queryAllTRU).


### Organizations

The network conssists of a manufacturer, third party logistics companies(3PL), distributer and maintanence&repair(M&R) organization. 

Manufacturer: Manufacturer is an OEM that produces parts for the market. When the parts are produced, the GTIN is recorded that includes the manufacturer ID.

Distributor: Distributor gets parts from the market, mostly manufacutrers, and sells them to the other parties.

3PL: 3PLs also buys and sells the parts. Additionally they can perform maintenance work on the parts and install them.

M&R: M&R organizations installs parts on the aerospace systems.

As new organizations are added thay are included in the blockchain and assigned a unique ORGID. Organizations may have certificates.

### Traceable REsource Unit (TRU)

Each traceable part grouping is called a Traceable Resource Unit(TRU) and identifiable by a unique id(TRUID) assigned in the blockchain. 

The history of TRU is stored in the TRACE entries. TRACE entries are stored per TRU and organization.

The transactions modify the TRU and TRACE entries.


### The User Interface 


### Create Part 

Part creations is done through createTRU transaction. This is coupled to manufacturing and testing of the TRU. As a manufacturer completes the process, he creates the part in the blockchain by assigning necessary details.


### Part Operations (updateTRU, splitTRU) 


### Ownership Change (QR code, shipTRU, changeOWN)


### Dispute Resolution (CreateDispute, RespondDispute, closeDispute)


### Use Case 1: Back-to-Birth Trace


### Use Case 2: Dispute Resolution through Consistent/Trusted Common Trace


### Use Case 3: Access Controlled Trace Data


### Potential Use Case: Tracking, Payment Notice and Performance Metrics






```markdown
Syntax highlighted code block



**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).


## Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
