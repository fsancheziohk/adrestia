# Adrestia

Adrestia is a product team working on developing tooling and client interfaces around Cardano. Our mission is to create an easier bridge between end-users applications and Cardano core node by pushing out higher level interfaces to interact with the Cardano blockchain.

This repository acts as a catalog of projects that fall under the scope of Adrestia. Checkout the [📘 Adrestia user-guide](https://input-output-hk.github.io/adrestia/) for more information!


# Architecture Overview


```
                                                      Adrestia
                                              <======================>

                                                +-----------------+        Daedalus
                                                |                 | HTTP   Exchanges
+--------------+ node-to-node               +-->+  cardano-wallet +------> Atala Prism
|              |                            |   |                 |        Dashboards
| cardano-node <---+                        |   +-----------------+        ...
|              |   |                        |
+------^-------+   |                        |
       |           |                        |
       |           |                        |
       |    +------v-------+                |   +-----------------+
       +    |              | node-to-client |   |                 | HTTP   Explorer v2
      ...   | cardano-node +--------------------> cardano-graphql +------> Exchanges
       |    |              |                |   |                 |        Pool Operator Tool
       |    +------^-------+                |   +-----------------+        ...
       |           |                        |
       |           |                        |
+------v-------+   |                        |
|              |   |                        |   +-----------------+
| cardano-node <---+                        |   |                 | HTTP   Explorer v1
|              |                            +--->   cardano-rest  +------> Exchanges
+--------------+ node-to-node                   |                 |        ...
                                                +-----------------+


                                              <======================>
                                                      Adrestia
```

# APIs

name / link       | description                                    | Byron              | Jörmungandr        | Shelley
---               | ---                                            | ---                | ---                | ---
[cardano-wallet]  | JSON/REST API for managing UTxOs in HD wallets | :heavy_check_mark: | :heavy_check_mark: | :construction:
[cardano-rest]    | JSON/HTTP API for browsing on-chain data       | :heavy_check_mark: | :x:                | :construction:
[cardano-graphql] | GraphQL/HTTP API for browsing on-chain data    | :heavy_check_mark: | :x:                | :construction:


# Libraries

Name / Link                 | Description                                                              | Haskell            | JavaScript
---                         | ---                                                                      | ---                | ---
[bech32]                    | Human-friendly Bech32 address encoding                                   | :heavy_check_mark: | [bitcoinjs/bech32](https://github.com/bitcoinjs/bech32)
[cardano-addresses]         | Addresses and mnemonic manipulation & derivations                        | :heavy_check_mark: | :construction:
[cardano-coin-selection]    | Coin selection and fee balancing algorithms                              | :heavy_check_mark: | :construction:
[cardano-launcher]          | Shelley cardano-node and cardano-wallet launcher for NodeJS applications | :x:                | :heavy_check_mark:
[cardano-serialization-lib] | Binary serialization of on-chain data types                              | :construction:     | :construction:
[cardano-transactions]      | Transaction construction and signing                                     | :heavy_check_mark: | :construction:

# Formal Specifications 

Name / Link                 | Description                                       
---                         | ---                                               
[utxo-wallet-specification] | Formal specification for a UTxO wallet            

# Internal

> :warning: Here be dragons. These tools are used internally by other tools and
> does not benefit from the same care in documentation than other tools above.

name / link        | description
---                | ---
[cardano-js]       | (experimental) Cardano primitives for ECMAScript applications
[cardano-js-sdk]   | (experimental) Cardano SDK for ECMAScript applications
[persistent]       | Fork of the persistent Haskell library maintained for cardano-wallet


[cardano-wallet]: https://github.com/input-output-hk/cardano-wallet
[cardano-rest]: https://github.com/input-output-hk/cardano-rest
[cardano-graphql]: https://github.com/input-output-hk/cardano-graphql
[cardano-coin-selection]: https://github.com/input-output-hk/cardano-coin-selection
[cardano-addresses]: https://github.com/input-output-hk/cardano-addresses
[cardano-transactions]: https://github.com/input-output-hk/cardano-transactions
[cardano-serialization-lib]: https://github.com/Emurgo/cardano-serialization-lib 
[bech32]: https://github.com/input-output-hk/bech32
[utxo-wallet-specification]: https://github.com/input-output-hk/utxo-wallet-specification
[cardano-launcher]: https://github.com/input-output-hk/cardano-launcher
[cardano-js]: https://github.com/input-output-hk/cardano-js
[cardano-js-sdk]: https://github.com/input-output-hk/cardano-js-sdk
[persistent]: https://github.com/input-output-hk/persistent


