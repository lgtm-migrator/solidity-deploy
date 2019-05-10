# solidity-deploy
[![npm version](https://badge.fury.io/js/solidity-deploy.svg)](https://badge.fury.io/js/solidity-deploy)

solidity-deploy is an npm module which allows someone to create custom contract deployment scripts, including an abstracted compiler and flattener. Ideally, it also allows for smart contracts to be verified on Etherscan smoothly (still buggy).

## Descripton
Currently structured as a node module, with tests passing; however, there are a number of changes this project will go through, including but not limited to:
- Addition of proper mocha tests (tests at this point are limited to a .sh script and mini-node script which runs deployments and flattening, respectively.)
- API documentation

At the moment, the module is currently reliant on [truffle-flattener](https://www.npmjs.com/package/truffle-flattener) for flattening; however, in the future, this will be phased out for a more general flattener, or at least give the user some choice on which flattener to use. 

Verification is still very buggy, needs success cases of verification via [Etherscan's Contract API](https://rinkeby.etherscan.io/apis#contracts). The class holding Etherscan verification (verify/etherscan-verify.js) may not be up to date with a few things on the rest of repository (may work in a vacuum, but not optimized for the module as a whole)

The general entry point of this module offers both initialization of a `SolidityDeploy` object, or access to any of the other classes directly. The advantage of using a `SolidityDeploy` object is avoiding repetition in passing options/config; the object supplies functions with the `create` prefix which handles this minimized 

## Mirror
A mirror of this repository is available at: https://serebii.io:2501/Luiserebii/solidity-deploy

## Credits
Thanks to those generous developers who entertained my questions, and helped me understand npm module design better!
* [clemlak](https://github.com/clemlak)
* <a href="https://github.com/d1ll0n"><img src="https://i.imgur.com/5xXlQDX.png"/></a>
