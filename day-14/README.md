## Fourteenth day of learning solidity

Read the official Solidity [documentation](https://docs.soliditylang.org/en/v0.8.9/)

### WILT

- contracts need to be marked as abstract when at least one of their functions is not implemented. Contracts may be marked as abstract even though all functions are implemented.
- if a contract inherits from an abstract contract and does not implement all non-implemented functions by overriding, it needs to be marked as abstract as well.
- function types revisited - different from function without implementation even though their syntax is similar. Example of function declaration (function without implementation): `function foo(address) external returns (address);`. Example of a declaration of a variable whose type is a function type `function(address) external returns (address) foo;`
- interfaces. Restrictions:
  - cannot inherit from other contracts, but can inherit from other interfaces.
  - all declared functions must be external.
  - cannot declare a constructor.
  - cannot declare state variables.
  - cannot declare modifiers.
- functions declared in interfaces are implicitly `virtual` and any functions that override them do not need the `override` keyword.
- interfaces can inherit from other interfaces. This has the same rules as normal inheritance.
- when library funnctions are called, their code is executed in the context of the calling contract. i.e `this` points to the calling contract.
