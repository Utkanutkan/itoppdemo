# Welcome to Traceability Blockchain Prototype

## Introduction

This is the repository for traceability blockchain prototype demonstration. This repository includes three different folder. Tracegui includes the tracegui application, traceapp includes the traceapi and trace conctract, external includes the external to access the traceapi from another client.

The installation instructions are tested on Ubuntu 20.04 LTS with a configuration of 2 GB RAM. 

```markdown

```
## Installation

You should install Hyperledger Fabric 1.4.4 first. The detailed installation instructions for this is given in Fabric page. After installing the fabric you need to run a simple network and install the standartparts smart contract.

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

##


```markdown
Syntax highlighted code block



**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Utkanutkan/itoppdemo/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
