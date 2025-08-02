# Mint Request Schema
This document describes all TCP request types that a mint must accept.

In Meadow, a mint request is a basic JSON array.

## Request types
* `SYNC` - synchronise funds to a wallet
* `SEND` - make a transaction from one wallet to another
* `HEALTH` - mint health check

## Examples
```
client> ["HEALTH"]
server> ["READY"]

client> ["SYNC"]
server> ["SYNCED", 45]

client> ["SEND", "<public key>", "<request signature>", 100]
server> ["SENT", "<public key>", 100]
```
