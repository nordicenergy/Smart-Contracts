
# Nordic Energy Platform:
----------------------



## Blockchain Stack:
-----------------
## Nordic Energy´s PowerChain is a blockchain-based IoT-platform consists of two parts; JavaScript app and eosio blockchain: 

•	JavaScript Stack:  ReactJS, Redux, NodeJS, Webpack

•	Blockchain Stack: EOSIO , IPFS, NODEOS, C++, ABI, Scatter

Users interact with the UI in client and sign the transaction in frontend. The signed transaction is sent to the blockchain directly. After the transaction is accepted in blockchain, the note is added into the multi index table in blockchain.



#### What is Blockchain?

Blockchain is a decentralized, distributed store of transaction data. Periodically a new block of transactions is created and connected to the previous block. It is distributed because the blockchain stores transactions across many computers. It is decentralized because the blockchain infrastructure is not owned by one company. Blockchain provides trust; cryptography and consensus ensures that transactions are immutable. Blockchain provides resilience and transparency; decentralization and distribution mean many copies of the blockchain are available for all to see.


## EOSIO
-----------------
The EOSIO software introduces a new blockchain architecture designed to enable vertical and horizontal scaling of decentralized applications. It differs from other blockchains by using features such as DPos as the consensus algorithm and staking for resource allocation. The software provides accounts, authentication, databases, asynchronous communication, and the scheduling of applications across multiple CPU cores and/or clusters. The resulting technology is a blockchain architecture that has the potential to scale to millions of transactions per second, eliminates user fees, and allows for quick and easy deployment of decentralized applications.

 

## What is a Smart Contract?
--------------------------
An EOSIO Smart Contract is software registered on the blockchain and executed on EOSIO nodes. Smart Contracts implement the semantics of a "contract" and action requests are automatically stored on the blockchain. The Smart Contract defines the interface (actions, parameters, data structures) and the code that implements the interface. The code is compiled for WebAssembly, that nodes can execute.


#### Features of EOSIO.

	High Throughput and Scalability
	Faster Confirmations and Lower Latency
	Feeless and Cost Predictable Blockchain
	Comprehensive Permission Schema
	Upgradability
	Less energy consumption
	Programmable Economics and Governance



## Building an EOSIO Smart Contract
----------------------------------
Smart contract source code can be written in any language that the WASM (WebAssembly) compiler supports, EOSIO currently supports the C languages (C/C++).


#### Transactions and Actions:

A contract and an account communicate in the form of actions. Actions can be sent individually, or batched together if they are intended to be executed atomically. The difference between an action and a transaction is that an action represents a single operation, whereas a transaction is a collection of one or more actions.

#### Smart Contract/CDT:

EOSIO.CDT is a toolchain for WebAssembly (WASM) and set of tools to facilitate contract writing for the EOSIO platform. In addition to being a general purpose WebAssembly toolchain, EOSIO specific optimizations are available to support building EOSIO smart contracts.

#### Nodeos:
Nodeos is the core EOSIO node daemon. Plugins can be used to configure nodeos to execute with various features. Nodeos handles all peer-to-peer networking, contract code scheduling, and the blockchain data persistence layer.

####Cleos/Keosd:
Keosd is a key manager for EOSIO accounts that comes with EOSIO. Cleos is a command-line tool which let developers interact nodeos as well as deploy, test EOSIO smart contracts.
 

## EOSJS
-------
A Javascript API SDK for integration with EOSIO-based blockchains using the EOSIO RPC API.


#### Scatter:

Scatter wallet for digital currencies and assets. It’s a multi-blockchain signature, identity, and reputation provider for Windows, Mac, Linux, Android, and iOS


## Smart Contract Integration:
----------------------------
EOS API service is created for integrating frontend component with our smart contract. We'll also be setting up Redux, which will keep a store of information for us so that we don't need to keep asking the blockchain every time we need the logged in user's name and other information. 

Redux will use what we call reducers to handle actions that modify the Redux store of state information.



## Quick start - Run the DApp
----------------------------

docker stop eosio_evcharging_container
docker start eosio_evcharging_container

Install Docker: https://docs.docker.com/docker-for-mac/install/ 
Install Node.js: https://nodejs.org/en/
 
#### Build process:

npm i
npm start



