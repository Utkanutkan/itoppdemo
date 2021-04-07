# Welcome to Traceability Blockchain Prototype

## Introduction

This is the repository for traceability blockchain prototype. The repository has three folders. Tracegui includes the tracegui application, traceapp includes the traceapi and standardparts contract, external includes the code to access the traceapi from another client.

The installations were tested on Ubuntu server 20.04 with a configuration of 2 GB RAM. It is recommended to start with a fresh instalallation.

## Installation

The prototype uses the Hyperledger Fabric 1.4. The detailed installation instructions is given in Hyperledger Fabric page(https://hyperledger-fabric.readthedocs.io/en/release-1.4/prereqs.html). After installing the fabric you need to run first network and install the standartparts smart contract.

```markdown
sudo apt install curl
sudo apt  -get -y install docker compose
sudo usermod -aG docker $USER
```
Restart and login again after docker installation. 

```markdown
sudo apt install curl
sudo apt  -get -y install docker compose
sudo usermod -aG docker $USER
```
The go programming language is installed and path variable is updated.
```markdown
wget -c https://dl.google.com/go/go1.12.17.linux-amd64.tar.gz -O - | sudo tar -xzf
export GOPATH=$HOME/go
```
Node.js version 8.9 to be installed as recommended. 

```markdown
curl -sL https://deb.nodesource.com/setup_8.9 -o nodesource_setup.sh
```

If you are using older version of linux such as 16.04 install python.

```markdown
sudo apt-get install python
sudo bash nodesource_setup.sh
sudo apt install nodejs
```
Check the versions of the prerequests.
```markdown
docker -v
docker-compose -v
go version
node -v
npm -v
```
Get the image of the fabric.

Copy the smart contract from the repository.

Start the network.

Copy the server files.

Start the server application.

Copy the client files.

Start the client application.

## Prototype Architecture, starting traceapi and tracegui
The traceapi is a node.js application. Ideally every organization runs a copy of their api. The blockchain api uses wallet and blockchain network configuration to access the blockchain. In the current configuration organizational wallet is included in the api. The tracegui is a vuetify application and calls the api functions.

1. Run the existing blockchain network.
2. Run the api server.
3. Run the client application.




First the API files are copied to your machine. In the server directory first the npm is intalled and server is run. 

```markdown
npm install
npm start
```

The client gui is also coped to folder in the aerver machine. The configuration of the api should be present in the client gui. The client web applicaiton is built and started. 

```markdown
npm install
nnpm run serve
```


```markdown

```
.Finally check the application from the you browser. The initial three parts that ecist in the initial contract can be seen/

```markdown

```

## The Scenario

The scenario is run on a presinstalled tracegui, traceapp and blockchain[itopp.nl/ORGID](itopp.nl/ORG1). See external access for calling api from python by connecting server [partsledger.tk/transactionname](partsledger.tk/queryAllTRU).


### Organizations

The network conssists of a manufacturer, third party logistics companies(3PL), distributer and maintanence&repair(M&R) organization. 

Manufacturer: Manufacturer is an OEM that produces parts for the market. When the parts are produced, the GTIN is recorded that includes the manufacturer ID.

Distributor: Distributor gets parts from the market, mostly manufacutrers, and sells them to the other parties.

3PL: 3PLs also buys and sells the parts. Additionally they can perform maintenance work on the parts and install them.

MRO: MRO organizations installs parts on the aerospace systems.

As new organizations are added thay are included in the blockchain and assigned a unique ORGID. Organizations have certificates.

For the tutorial example, we work on a network with six organizations.


```markdown
![image](/assets/images/blockchainorgs.jpg)
```

### Traceable Resource Unit (TRU)

Each traceable part grouping is called a Traceable Resource Unit(TRU) and identifiable by a unique id(TRUID) assigned in the blockchain. 

The history of TRU is stored in the TRACE entries. TRACE entries are stored per TRU and organization.

The transactions modify the TRU and TRACE entries.

```markdown
![image](/assets/images/truandtrace.jpg)
```

### The User Interface 


### Create Part 

Part creations is done through createTRU transaction. This is coupled to manufacturing and testing of the TRU. After manufacturer completes the manufacturing,  cre in the blockchain by submitting 


### Part Operations (updateTRU, splitTRU) 


### Ownership Change (QR code, shipTRU, changeOWN)


### Dispute Resolution (CreateDispute, RespondDispute, closeDispute)


### Use Case 1: Back-to-Birth Trace

You can see the trace of the TRU6 for the M&R organization. It includes every operation the part has gone through from naufacturing.



### Use Case 2: Dispute Resolution through Consistent/Trusted Common Trace

The trace data for TRU6 for M&R and the supplier is shown respectively. So the supplier trace is the same as the trace of M&R organization accept the latest operations. The supplier can see the exact problem as reported as dispute and take action. 



### Use Case 3: Access Controlled Trace Data

The trace data can be modified by the owner organization and not the others. Upon shipping, only getOWN transaction can be called first. After this trace data is owned and modified by the current owner only.


### Use Case 4: Payment Notice 





```markdown
Syntax highlighted code block



**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).


## Summary of Transactions

![image](/assets/images/transactions.jpg)


## Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
