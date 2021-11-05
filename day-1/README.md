## First day of learning solidity

Learned a bit about the basics of the language via building a zombies game on [crypto zombies](https://cryptozombies.io/).

**these might be a little incorrect as they are based on my observation and understanding**

### WILT

- `struct`. A little strange in that it's a lot like interfaces in typescript - a data type that exists to describe the shape of data and to provide type annodations for these non-primitive data types. Except that structs are callable and functions as a way to create the object inn the shape of the struct.
- solidity does not have native string comparison. To compare strings of the same length, you would have to compare their `keccak256` hashes. According to [this link](https://ethereum.stackexchange.com/a/68069), it is because strings aren't really primitives in solidity.
- you can restrict execution of a function depending on the fulfilment of certainn conditions by using `require(CONDITION)`.
