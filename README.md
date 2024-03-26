# Messages and Eth saver webAPP

This project demonstrates a basic Hardhat use case. 
It has 2 contracts, a test for each contract, and a script that deploys the contracts.

## Contracts

### WavePortal.sol
In summary, this contract allows users to send messages to it, stores those messages along with some metadata, and allows anyone to retrieve all the messages or the total count of messages.


### Lock.sol
This Ethereum smart contract, named Lock, acts like a digital time-locked safe.

When the contract is created, it's assigned an unlockTime (a future point in time) and an owner (the person who creates the contract). The contract can also receive Ether during its creation due to the payable keyword in the constructor.

The contract has a withdraw function that allows the owner to withdraw all the funds from the contract, but only if the current time is equal to or later than the unlockTime. If these conditions are not met, the withdrawal attempt will fail with an error message.

In essence, this contract allows someone to store Ether in it until a specified future time, at which point the Ether can be withdrawn by the owner.

## Scripts

### Deploy
This script is used to deploy the `WavePortal` smart contract to the Ethereum blockchain using the Hardhat development environment.

### Run
This script deploys the WavePortal contract, sends a couple of waves to it from different accounts, and retrieves and logs the total number of waves and all the waves.


Use npx for run scripts, example:

```shell
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat run scripts/deploy.js
```
