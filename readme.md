# mining tuturial monero (xmr)

## What is crypto mining and how does it work? 

Crypto currency is a reliable way of verifying and storing reliable transactional data. Instead of having for example two banks storing all the information about transactions, every single miner is storing their own copy of all transactions ever made of a single crypto currency. 

A transactional data point is called a block. Many blocks are called a blockchain. With mining the computer is trying to solve a puzzle what allow to contribute to the block chain and in return get rewareded with a certain amount of crypto currencies.

### What is monero?

Monero is a crypto currency and is made in a way that allows much less powerful machines to have a better change against more powerful machines. This mechanism is built into monero. 

### Hardware setup

* Raspberry Pi5 8GB 
* use Raspberry Pi Imager
* OS: Raspbian OS 64-Bit -> flash it to a usb hard drive
* choose hostname and password to control Raspberry Pi remotely via putty
* put the usb hard drive in the Raspberry Pi and boot it up

### Software setup 

* update the computer with: `sudo apt -y update && sudo apt -y upgrade`
* install mining software: `sudo apt install git build-essential cmake libuv1-dev libssl-dev libhwloc-dev -y`
* cloning xmrig: `git clone https://github.com/xmrig/xmrig.git`
* change directory into the downloaded folder: `cd xmrig`
* navigate into the build folder: `cd build`
* execute cmake: `cmake ..`
* compile software from source `make`

### Crypto wallet

To send and receive crypto currencies a wallet is needed. Install a wallet:

e.g. https://mymonero.com/

* create new wallet

#### execute xmrig

Consider either solo or pool mining. In this tutorial an example for pool mining is given.

`./xmrig -o gulf.moneroocean.stream:10128 -u <wallet-address> -p <miner-alias>`

show infos: 

* hit `h` hash rate
* hit `s` check result
* hit `c` check connection

