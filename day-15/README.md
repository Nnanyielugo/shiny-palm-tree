## Fifteenth day of learning solidity

Following Andrei Dumitrescu's course on [udemy](https://www.udemy.com/course/master-ethereum-and-solidity-programming-with-real-world-apps)

### WILT

- ethereum nodes, types: full node, light node and archive node.
- ethereum accounts, types: externally owned account(user account) and contract account.
- ethereum account components
  - nonce
  - balance(in wei)
  - account address
  - account private and pubblic key(only for EOA)
  - code(only for contract account). This is the immutable EVM bytecode.
  - storage(only for contract account). Empty by default.
- an EOA address is derived from the last 20 bytes(160 bits) of the public key that are `keccak256` hashed. It's represented in a hexadecimal format which is often indicated explicitly by appending `0x` to the address.
- the address for an ethereum contract is deterministically computed from the address of its creator(sender) and the number of transactions the creator has sent (nonce).
- private key ownership of crypto accounts.
- cold storage and eth account security.
- where to request test eth from.
- offline signing of eth transfer request.
- gas price, gas limit and opcodes.
- types of nonce:
  - block nonce
  - externally owned account nonce
  - contract nonce
