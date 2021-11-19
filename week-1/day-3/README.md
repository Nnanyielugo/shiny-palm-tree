## Third day of learning solidity

Still learning on [crypto zombies](https://cryptozombies.io/). On lesson 3.

### WILT

- ownable contracts.
- contract ownerships can be set using constructors - which makes sense seeing as contracts are immutable and run forever and constructors can be called only once - when the conntract is first created.
- function modifiers.
- gas, gas cost, code optimization to reduce cost of executing contracts on Ethereum.
- gas saving techniques:
  - struct packing.
  - cluster identical data types in structs.
  - use view functions where possible. View functions don't cost any gas when they're called externally by a user.
  - storage is expensive. Avoid writes unless absolutely necessary.
  - looping over large (and small) data sets is cheaper than using storage if it's in an external view function, since view functions don't cost your users any gas.
  - create variables in memory rather than storage if they will not exist beyond the end of the function call.
- can pass a storage pointer to a struct as an argument to a private or internal function.
- more on data locations - calldata.
