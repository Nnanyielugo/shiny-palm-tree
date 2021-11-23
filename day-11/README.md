## Eleventh day of learning solidity

Read the official Solidity [documentation](https://docs.soliditylang.org/en/v0.8.9/)

### WILT

- enums extended: default values.
- function extended: function types.
- reference types: data location contd: `memory`, `storage`, and `calldata`.
- concatenate two strings using `bytes.concat(bytes(s1), bytes(s2))`.
- reminder: you can also compare two strings by their keccak256-hash using `keccak256(abi.encodePacked(s1)) == keccak256(abi.encodePacked(s2))`.
- you should use `bytes` over `bytes1[]` because it is cheaper, since `bytes1[]` adds 31 padding bytes between the elements.
- as a general rule, use `bytes` for arbitrary-length raw byte data and `string` for arbitrary-length string (UTF-8) data.
- declaring a `struct` outside a contract allows it to be shared among multiple contracts.
