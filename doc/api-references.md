API References
==============

## Components


* [cardano-wallet](https://input-output-hk.github.io/cardano-wallet/api/edge)
* [cardano-submit-api](https://input-output-hk.github.io/cardano-rest/submit-api/)
* [cardano-explorer-api](https://input-output-hk.github.io/cardano-rest/explorer-api/)
* [cardano-graphql](https://input-output-hk.github.io/cardano-graphql/)

> **HINT**:  _About cardano-wallet_

Cardano-wallet comes with a command-line interface that can be used as a quick alternative to cURL or wget to interact with a server running on localhost. Every endpoint of the API is mapped to a corresponding command which often offers a better user experience than directly interacting with the API as a human (API are for programs, command-lines are for humans).

For example, restoring a wallet goes normally through `POST /byron-wallets`, or can be done interactively with

```
$ cardano-wallet wallet create MyWallet
```

The command line also provides some useful helpers like a command to generate mnemonic sentences, or doing key derivation. For more details, see the wallet command-line user manual.


## Libraries

| Library                                                                             | Haskell                                                           | JavaScript                              |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------|
| [cardano-addresses](https://github.com/input-output-hk/cardano-addresses)           | <https://input-output-hk.github.io/cardano-addresses/haddock/>      | _Soon available._                       |
| [cardano-transactions](https://github.com/input-output-hk/cardano-transactions)     | <https://input-output-hk.github.io/cardano-transactions/haddock/>   | _Soon available._                       |
| [cardano-coin-selection](https://github.com/input-output-hk/cardano-coin-selection) | <https://input-output-hk.github.io/cardano-coin-selection/haddock/> | _Soon available._                       |
| [bech32](https://github.com/input-output-hk/bech32)                                 | <https://input-output-hk.github.io/bech32/haddock/>                 | See <https://github.com/bitcoinjs/bech32> |

About cardano-transactions
--------------------------

In addition to the low-level library, cardano-transactions also provides a command-line interface (`cardano-tx`) to construct transactions directly in the terminal.
Check out the repository's documentation and examples to see example usage.

[cardano-wallet]: https://github.com/input-output-hk/cardano-wallet
[cardano-rest]: https://github.com/input-output-hk/cardano-rest
[cardano-graphql]: https://github.com/input-output-hk/cardano-graphql
