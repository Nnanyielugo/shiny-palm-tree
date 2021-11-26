## Learning solidity Week 1
*You can check the individual day journals to get more information*

I got a recommendation to a [crypto zombies](https://cryptozombies.io/) tutorial and spent the entire week on their tutorial on how to build a zombies game.

During this time, I learned about `structs` and how it is similar in some ways to typescript’s `interfaces`, but different in that it is used to create the object it models, and properties are passed as positional arguments.

I learned about how strings aren’t exactly primitives in solidity and how string comparison have to be done by comparing their `keccak` hashes instead of the strings themselves. Numbers do not have this restriction.

I learned that function executions can be restricted depending on set conditions, similar to using conditionals, except these can be used to create reusable function modifiers and automatically throw errors if the set conditions are not met.

I learned that contracts deployed on the EVM are immutable and how to get around the restrictions it imposes to be able to modify critical logic - quite simply, avoiding magic strings and hardcoded values - which most experienced devs know to do in other languages anyway. I learned about transactions cost - gas, and about gas saving techniques.

I learned about tokens, and the most important difference between cryptocurrencies and crypto-collectibles (NFTs).

Last thing I learned were about JSON-RPC, contract ABIs, setting up metamask, and web3.js
