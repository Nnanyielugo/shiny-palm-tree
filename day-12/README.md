## Eleventh day of learning solidity

Read the official Solidity [documentation](https://docs.soliditylang.org/en/v0.8.9/)

### WILT

- the key data is not stored in a mapping, only its keccak256 hash is used to look up the value.
- mappings can only have a data location of storage and thus are allowed for state variables, as storage reference types in functions, or as parameters for library functions. They cannot be used as parameters or return parameters of contract functions that are publicly visible. These restrictions are also true for arrays and structs that contain mappings.
- you cannot iterate over mappings, i.e. you cannot enumerate their keys
- iterabe mappings
- `delete a[x]` deletes the item at index x of the array and leaves all other elements and the length of the array untouched. This especially means that it leaves a gap in the array.
- reassigning variables inside functions will behave produce different behavior depending on the reference type of the source and the target.
- assignments to local variables referencing storage objects can only be made from existing storage objects. assignments here also includes delete statements since `delete` in solidity for the most part, simply means assigning to that variable the minimum value of its type.
- explicit conversions from `bytes20` or any integer type to `address` result in `address payable`.
