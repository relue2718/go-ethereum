.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/relue2718/go-ethereum/cmd/swarm
	go build -o bin/geth     github.com/relue2718/go-ethereum/cmd/geth
	go build -o bin/bootnode github.com/relue2718/go-ethereum/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/relue2718/go-ethereum/swarm/...
