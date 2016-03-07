# hightps

## DACH
### Build docker image
```
	git clone
	cd dach
	docker build -t dach .
```
### Run docker container
#### Daemon
```
	docker run -d dach
```
#### Interactive shell
```
	docker run -it dach /bin/bash
```
So far all I can get out of this is "Started successfully", not sure what the next step is

## IBM

Installed locally on my machine following [instructions](https://github.com/openblockchain/obc-docs/blob/master/dev-setup/devenv.md) (Had to enable virutalization in BIOS).
GOPATH envvar was set with `export GOPATH=$HOME/go`
Ended up with two directories
```
  ~/go/src/github.com/openblockchain/obc-peer
  ~/hightps/ibm/WORKSPACE
```
To start the peer
```
	cd hightps/ibm/WORKSPACE/obc-dev-env
	vagrant up
	vagrant ssh
```
Now inside the vagrant VM
```
	cd $GOPATH/src/github.com/openblockchain/obc-peer	
```
To start the peer
```
	./obc-peer peer
```
To use the [CLI](https://github.com/openblockchain/obc-docs/blob/master/api/Openchain%20API.md#open-blockchain-cli) `vagrant ssh` in another shell window and you can do things like
```
	curl localhost:5000/chain
	curl localhost:5000/chain/blocks/2	
	curl localhost:5000/network/peers
	curl localhost:5000/transactions/bb540edfc1ee2ac0f5e2ec6000677f4cd1c6728046d5e32dede7fea11a42f86a6943b76a8f9154f4792032551ed320871ff7b7076047e4184292e03421889c
```