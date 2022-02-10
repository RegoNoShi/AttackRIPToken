# RIPToken Exploit

Exploit a smart contract that uses a "random" function to decide how many token to mint. The technique used is similar to what is used to pass the **Predict the future** challenge of the[CaptureTheEther](https://capturetheether.com/) project.

The original RIPToken was implemented by [Mr RIP](https://mr.rip) during one of his [Coding In Public sessions](https://youtu.be/zF3KaEqpOxg) and is deployed [here](https://ropsten.etherscan.io/address/0xa475cb9264a74c9e2307b8516db1ddc1bc1ea952).

## Pre-requisites:

1. Checkout the repo
2. Install [Python](https://www.python.org/downloads/) (I'm using Python 3.9.10)
3. Install [Brownie](https://eth-brownie.readthedocs.io/en/stable/install.html)
4. To exploit the real contract or to test on tesnet (eg. kovan, ropsten, etc.):
   1. Create a `.env` file in the root folder. Example file [here](.env.example)
   2. Add an entry in the `.env` file to set the private key of the account to use `export PRIVATE_KEY=<your private key here>`
   3. Add an entry in the `.env` file to set the [Infura](https://infura.io/dashboard) projectId to use `export WEB3_INFURA_PROJECT_ID=<your infura projectId here>`

## Try the exploit:

Use `brownie run exploit` to test the exploit locally or `brownie run exploit --network ropsten` to exploit the real contract.

Note: the default amount used is 0.1 ether. You can change the amount to use at the beginning of the [exploit.py](exploit.py) script.
