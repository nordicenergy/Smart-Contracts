CPP_IN=stablecoin
CLEOS=$(CLEOS)
CONTRACT_ACCOUNT=nordicenergy
CLEOS=cleos -u http://api.kylin.alohaeos.com

build:
	eosio-cpp -abigen $(CPP_IN).cpp -o $(CPP_IN).wasm

all: build

deploy: build
	$(CLEOS) set contract $(CONTRACT_ACCOUNT) ../stablecoin -p nordicenergy

pause:
	$(CLEOS) push action $(CONTRACT_ACCOUNT) pause '{}' -p nordicenergy

transfer:
	$(CLEOS) push action $(CONTRACT_ACCOUNT) transfer '{"from":"stablecoin", "to":"nordicenergy",  "quantity":"1,000,000,000 NSC", "memo":"energy asset"}' -p nordicenergy

clean:
	rm -f $(CPP_IN).wast $(CPP_IN).wasm


#cleos -u http://kylin-testnet.jeda.one:8888 push action stablecoim create '{"issuer":"nordicenergy", "maximum_supply":"10000 NSC"}' -p nordicenergy