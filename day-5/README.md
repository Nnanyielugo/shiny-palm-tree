## Fourth day of learning solidity

Still learning on [crypto zombies](https://cryptozombies.io/). On lesson 5.

### WILT

- tokens on Ethereum
  - fungible (cryptocurrencies) and non-fungible(NFTs) (crypto-collectibles) tokens.
  - ERC-20 - blockchain-based assets that have value and can be sent and received. - suitable for tokens act as cryptocurrencies.
  - ERC721 tokens. - not interchangeable since each one is assumed to be unique (non-fungible), and are not divisible. You can only trade them in whole units, and each one has a unique ID. - suitable for crypto-collectibles. More on non-fungible tokens [here](https://www.nftically.com/blog/what-are-crypto-collectibles-uses-of-nfts-in-crypto-collectibles/).
- implementing a token contract.
- contract can inherit from multiple contracts in solidity.
- implementing ERC721.
- libraries in solidity.
- preventing underflows and overflows - using SafeMath.
- code commenting and the natspec standard. (@notice, @author, @title, @dev, @return, @param).

### lesson 6

### WILT

- JSON-RPC
- web3.js
- ethereum (and blockchains in general) use a public / private key pair to digitally sign transactions.
- Metamask.
- contract address
- contract ABI - Application Binary Interface.
- web3.js contract functions - call, send, and payable.
- wei - the smallest sub-unit of Ether — there are 10^18 wei in one ether.
- using indexed - filter events and only listen for changes related to the current user.
- querying past evennts using getPastEvents().
- using events as a cheaper form of storage. Has tradeoffs though.
