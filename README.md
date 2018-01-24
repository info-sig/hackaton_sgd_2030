# Introduction

Our aim is to allow municipalities to issue self-mintable utility tokens for
basic goods.

The municipalities (service providers) would issue tokens as a part of an UBI or similar
scheme and the clients would be free to use (burn) them in exchange of city services.

Note that the municipality doesn't need to own any infrastructure, the system as
designed now is operational *now* and can be deployed to the ETH swarm given enough ether.

Considering the process of development of ECR20 tokens is so straightforward the idea
is to develop tokens for each specific purpose, and give each token specific properties
that best fit it's role - transport, electricity, internet access... in it's particular
geographical location (transfer limits, any fees, option to trade or not - should be
chosen in communication with regional actors).

For example:

1. some tokens may be tradeable - either directly through the ETH network, or through 
a specialized wallet held by the service provider which has the capability to run
contracts as a wallet owner
2. most tokens will have the mintable property for the service provider - the idea 
here is the capability to attach a "PoW" to the minting process, ie "cleaning snow in the 
winter gives you X transport and Y internet access tokens"
3. used tokens will generally be burned or sank

To make this scheme useful to the general public - in public spaces such as trams, public keys can be put into [Mifare cards](https://en.wikipedia.org/wiki/MIFARE)
backed by a safe & centralized cryptographic (session-key based) scheme based on the DesFire EV2 chip
that has been developed in-house - those cards can be read by any NFC-capable device
with appropriate cryptographic keys. 

The system can be integrated with conventional banking interfaces and wallets as necessary using the FIAT bridge (jSecModule) which has also
been developed in-house.


# Instructions

First, check out our demo token on the [Ropsten test network](https://ropsten.etherscan.io/token/0x39dbb38e6d448ffd228534b21b9bf80e37d8fb3a)

## As a developer

1. [install the geth node](https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Ubuntu)
  1. use the provided script in `scripts/run_geth.sh` to run the node on the Ropsten test network
2. [install & run the Wallet](https://github.com/ethereum/meteor-dapp-wallet/tree/87ccad69413cbdbcde2a3006b9f7ff701767f576)
3. ...

## As a service provider

1. build the Wallet into static content and deploy it somewhere - you can use [ETH Swarm](https://medium.com/async-la/deploy-your-own-ethereum-blockchain-with-swarm-on-aws-bffc3d4dccc2), GH pages, S3, ... any place which allows you to host static files
2. 

## As a client

1. [install the Metamask chrome extension & follow instructions to set it up](https://metamask.io/) && connect it to Ropsten test network (top of the Metamask screen)
2. open the Wallet, it should be running on http://localhost:3000, but since at this point source code is shared with the meteor-dapp-wallet you can simply go to https://wallet.ethereum.org/ - your wallet should already be loaded and running via Metamask


# Future development

1. customize the contract to the specific first use case
2. setup simple scripts to deploy the wallet to the Swarm
3. tweak the Wallet to allow a more streamlined user experience (ie list the community tokens first by default and any ETH balances later)