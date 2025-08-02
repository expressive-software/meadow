# The Meadow Protocol

## Summary
Meadow is a decentralized payment processing protocol aimed at being uncensorable and less resource heavy.

* It does not rely on a blockchain or a peer-to-peer technology
* It's simple to implement
* It can't be censored
* It's end to end encrypted, thus making the transactions invisible for the mint vendor

## Glossary
* Wallet - a piece of software or hardware that stores Meadow funds
* Mint - a TCP server containing every registered wallet
* Banknote - a signed JSON string containing transaction metadata

## Protocol structure
```
----------                       ----------                       ----------
|        |                       |        |                       |        |
|WALLET 1| < - - - - - - - - - > |  MINT  | < - - - - - - - - - > |WALLET 2|
|        |                       |        |                       |        |
|        |                       |        |                       |        |
----------                       ----------                       ----------
```

The default port for a mint is `2222`

### Wallet structure
Wallets have a keypair and an address. 

Keypairs use the secp256k1 algorithm.

Addresses can be also pointed to a web domain by simply creating a file called `meadow` or `meadow.txt` inside of `.well-known` folder.

## License
[Public domain](LICENSE)
