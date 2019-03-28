## Create new Ethereum private network

# Create new node

1 - mkdir ~/ChainSkills/private
2 cd ~/ChainSkills/private
3 puppeth
4 2. configure new genesis
  1. Create new genesis from scratch
  1. Ethash proof of work
  0x type enter
  yes
  Nutwork ID :4224
  
5 export genesis as Json file
6 open file with atom
7 create node via geth using the genesis file : geth --datadir . init .\chainskills.json
 It generates geth => data
              keystore => account
			  
8 create new account : geth --datadir . account new
 => Address: {5a81ac7af671f6c9b42843b9b6cca0e00caf7b09}
 
9 list accounts : geth --datadir . account list

10 create file : atom startnode.cmd with :
geth --networkid 4224 --mine --minerthreads 1 --datadir "." --nodiscover --rpc --rpcport "8545" --port "30303" --rpccorsdomain "*" --nat "any" --rpcapi eth,web3,personal,net --unlock 0 --password ./password.sec

11 create password.sec containing the password
12  run script to start node


# connect to node

1 open new power shell and type : geth attach ipc:\\.\pipe\geth.ipc
2 eth.accounts => List all accounts
3 eth.coinbase
4 eth.getBalance(eth.coinbase)
5 eth.getBalance(eth.accounts[1])
6 web3.fromWei(eth.getBalance(eth.coinbase),"ether") => balance en eth du premier account
7 miner.stop()
8 miner.start(1) => mine on one thread
9 net.version => get network id
10 personal.unlockAccount(eth.accounts[1],"pass1234",300) => unlock account for 300 seconds 
to be able to sign transactions
11 eth.sendTransaction({from: eth.coinbase, to: eth.accounts[1], value: web3.toWei(10, "ether")})  =>
send eth from one account to another
