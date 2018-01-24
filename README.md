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

1. harden the contract
2. setup simple scripts to deploy the wallet to the Swarm
3. 
