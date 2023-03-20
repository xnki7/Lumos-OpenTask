This is a Solidity smart contract that implements an ERC721 non-fungible token (NFT) with additional functionalities such as pausing, burning, voting, and URI storage. The contract is named "Xnki7" and uses "XK7" as its symbol.

The contract imports various modules from the OpenZeppelin library, including ERC721, ERC721Enumerable, ERC721URIStorage, Pausable, Ownable, ERC721Burnable, ERC721Votes, and Counters. The Counters module is used to keep track of the token ID counter.

The contract's constructor sets the token name and symbol and initializes a domain separator. The contract owner can pause and unpause the contract using the pause() and unpause() functions, respectively.

The safeMint() function allows the owner to mint a new token and assign its URI. The function generates a new token ID using the Counters module, increments the counter, and assigns the token to the specified recipient.

The _beforeTokenTransfer() function overrides the corresponding functions in ERC721 and ERC721Enumerable, and ensures that token transfers can only occur when the contract is not paused.

The _afterTokenTransfer() function overrides the corresponding function in ERC721Votes and updates the voting status of the token after it is transferred.

The _burn() function overrides the corresponding functions in ERC721 and ERC721URIStorage, and allows the owner to burn a token.

The tokenURI() function overrides the corresponding function in ERC721URIStorage and returns the URI associated with a given token ID.

Finally, the supportsInterface() function overrides the corresponding functions in ERC721 and ERC721Enumerable, and checks whether a given interface is supported by the contract.
