## Hello world Contract


# With command Line

mkdir ~/ChainSkills/Training/Greetings
cd ~/ChainSkills/Training/Greetings
npm init
npm install web3@0.20.0 solc@0.4.18 => install libraries to compile smart contracts
atom Greetings.sol

contract Greetings {
  string message;

  function Greetings() public {
    message = "I am ready !";
  }

  function setGreetings(string _message) public {
    message=_message;
  }

  function getGreetings() public view returns (string) {
    return message;
  }
}

node => start node console
Web3 = require('web3') => load library
web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:7545")) => connect to ganache node
web3.eth.accounts
solc = require('solc') => load library for solidity
sourceCode = fs.readFileSync('Greetings.sol').toString()
compiledCode = solc.compile(sourceCode) => compile the code
contractABI = JSON.parse(compiledCode.contracts[':Greetings'].interface) => extract ABI
greetingsContract = web3.eth.contract(contractABI) => create contract factory
byteCode = compiledCode.contracts[':Greetings'].bytecode => get contract bytecode
greetingsDeployed = greetingsContract.new({data : byteCode, from : web3.eth.accounts[0],gas:4700000}); => deploy contract
greetingsDeployed.address => address of deployed contract
greetingsInstance = greetingsContract.at(greetingsDeployed.address) => get instance of deplyed contract
greetingsInstance.getGreetings()
greetingsInstance.setGreetings("Hello all ! ", {from:web3.eth.accounts[0]})


# with Truffle on in memory ganache node

mkdir -p  mkdir -p  ~/ChainSkills/Training/GreetingsTruffle
cd ~/ChainSkills/Training/GreetingsTruffle
truffle init
atom .

var Greetings = artifacts.require("./Greetings.sol");

module.exports = function(deployer){
  deployer.deploy(Greetings);
};

truffle develop => start dev mode
Open new terminal then  truffle develop --log => start log console
migrate --compile-all --reset => compile and deploy
Greetings.address
web3.eth.accounts
Greetings.deployed().then(function(instance) {app=instance;}) => get instance of contract and store it in app variable (https://scotch.io/tutorials/javascript-promises-for-dummies)
app.getGreetings()
.exit


# with Truffle on ganache

In truffle.js add a network :
networks: {
    ganache:{
      host:"localhost",
      port:7545,
      network_id:"*"
    }
truffle migrate --compile-all --reset --network ganache
truffle console --network ganache



# NB

ABI : application binary interface => defines what functions are available in the contract and how call them

Web3 with truffle commands : 
web3.eth.getTransaction(*trshash*) 
web3.eth.getBlock(*blockhash*)
web3.eth.sendTransaction({from : web3.eth.accounts[0], to : web3.eth.accounts[1], value : web3.toWei(5,"ether")}) => send 5 eth from one account to another

# Resources

https://etherscan.io/opcode-tool => tool used to decompile binary bytecode into corresponding opcodes executed by ethereum VM (each opcode has code in gas)
