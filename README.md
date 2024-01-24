# ass2_BTx
Title
Smart Contract Deployment and Interaction using web3.js and Metamask

Usage
This guide provides step-by-step instructions on configuring your environment to deploy and interact with a smart contract using web3.js and Metamask. The process involves setting up the environment, configuring web3.js with Ganache and/or a Public Testnet, configuring Metamask, deploying a smart contract, and finally, calling functions from the deployed smart contract.

npm install web3
var Web3 = require('web3');
var url = 'http://localhost:1614'; // Update with Ganache or Testnet URL
var web3 = new Web3(url);
var address = '0x000000000'
web3.eth.getBalance(address, (err, bal) => { balance = bal })
balance





![image](https://github.com/zhambyl14/ass2_BTx/assets/147126858/7c611156-7f2f-4a65-94ff-3ed5adf7373a)
![image](https://github.com/zhambyl14/ass2_BTx/assets/147126858/715e0daf-f525-49e8-be34-290b5ff0db40)
![image](https://github.com/zhambyl14/ass2_BTx/assets/147126858/886e42c3-4c16-4866-a48f-965b778db4d8)



Utilize web3.js to interact with the deployed smart contract. Example code:
var contractAddress = '0x...'; // Replace with the deployed contract address
var contractInstance = new web3.eth.Contract(abi, contractAddress);

// Example: Call a function from the smart contract
contractInstance.methods.yourFunction().call((err, result) => {
  if (!err) {
    console.log('Function result:', result);
  } else {
    console.error('Error calling function:', err);
  }
});
