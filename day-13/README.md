## Thirteenth day of learning solidity

Read the official Solidity [documentation](https://docs.soliditylang.org/en/v0.8.9/)

### WILT

- type conversion from non boolean to boolean types as done in languages like Javascript is not supported in solidity
- internal function calls are translated to simple jumps inside the EVM while external function calls (via `this.fn()` or `contractInst.fn()` where `contractInst` is is the current contract) use a message call.
- tuples are not proper types in Solidity, they can only be used to form syntactic groupings of expressions.
- using a custom error instance will usually be much cheaper than a string description, because you can use the name of the error to describe it, which is encoded in only four bytes. A longer description can be supplied via NatSpec which does not incur any costs.
- `if (!condition) revert(...);` and `require(condition, ...);` are equivalent as long as the arguments to `revert` and `require` do not have side-effects, for example if they are just strings.
- the `require` function is evaluated just as any other function. This means that all arguments are evaluated before the function itself is executed. In particular, in `require(condition, f())` the function `f` is executed even if `condition` is true.
- The `try` keyword has to be followed by an expression representing an external function call or a contract creation (`new ContractName()`).
- the default visibility level for state variables is `internal`.
- getter functions have external visibility. If the symbol is accessed internally (i.e. without `this`.), it evaluates to a state variable. If it is accessed externally (i.e. with `this`.), it evaluates to a function.
- a contract can have at most one `receive` function, declared using `receive() external payable { ... }` (without the `function` keyword). This function cannot have arguments, cannot return anything and must have `external` visibility and `payable` state mutability. It can be virtual, can override and can have modifiers.
- a contract can have at most one `fallback` function, declared using either `fallback () external [payable]` or `fallback (bytes calldata _input) external [payable] returns (bytes memory _output)` (both without the `function` keyword). This function must have `external` visibility. A fallback function can be virtual, can override and can have modifiers.
- you can add the attribute `indexed` to up to three parameters which adds them to a special data structure known as “topics” instead of the data part of the log. A topic can only hold a single word (32 bytes) so if you use a reference type for an indexed argument, the Keccak-256 hash of the value is stored as a topic instead.
- if you do not provide any parameters, the error only needs four bytes of data and you can use NatSpec to further explain the reasons behind the error, which is not stored on chain. This makes this a very cheap and convenient error-reporting feature at the same time.
- if a constructor takes an argument, it needs to be provided in the header or modifier-invocation-style at the constructor of the derived contract.
- for multiple inheritance, the most derived base contracts that define the same function must be specified explicitly after the `override` keyword. In other words, you have to specify all base contracts that define the same function and have not yet been overridden by another base contract (on some path through the inheritance graph).
- an explicit override specifier is not required if the function is defined in a common base contract or if there is a unique function in a common base contract that already overrides all other functions.
- public state variables can override external functions if the parameter and return types of the function matches the getter function of the variable.
- you can use internal parameters in a constructor (for example storage pointers). In this case, the contract has to be marked abstract, because these parameters cannot be assigned valid values from outside but only through the constructors of derived contracts.
