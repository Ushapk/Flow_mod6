
# NFT
This Cadence program implements the Non-Fungible Token standard for creating and managing NFTs. 
This program allows users to mint new NFTs, deposit and withdraw NFTs, and transfer ownership of NFTs between users.

## Description
There is a cadence contract that demonstrates the creation and management of non-fungible tokens (NFTs) using the standard NonFungibleToken library in the Flow blockchain. The contract allows for the creation of NFTs with metadata such as name, favorite food, and lucky number. 
It also includes functions for depositing, withdrawing, transferring, and borrowing NFTs with a given ID.
The CryptoPoops contract implements the NonFungibleToken standard and defines a resource called NFT for the creation of NFTs with custom metadata.
It also defines a Collection resource that allows for the management of a collection of NFTs owned by a given address.
The contract also includes a Minter resource for the creation of NFTs and minting them into a Collection.

PubMyCollection interface : Defines the public functions deposit(), getIDs(), borrowNFT(), borrowAuthNFT() and withdraw() used to interact with the collection resource.
createEmptyCollection() : Creates an empty collection.
createMinter() : Creates a minter resource for minting NFTs.

## How it works
#### Deploy the contract
* Compile the contract using the Cadence Compiler.
* Deploy the contracts "NFT_1.cdc" and "NFT_2.cdc" to the Flow network node.
* Create the collection with "Createcollection.cdc"
* Mint a new NFT with "DepositNFT.cdc"
* Use Scripts to display metadata of the NFT's

#### Functions Inside The Contract

* Withdraw an NFT

Call the getIDs() function on the Collection instance to get the list of NFT IDs you own.
Call the withdraw(withdrawID) function on the Collection instance and pass in the ID of the NFT you want to withdraw.
The NFT will be transferred back to the caller.

* Transfer an NFT

Call the borrowAuthNFT(id) function on the Collection instance and pass in the ID of the NFT you want to transfer.
Create a new instance of the Collection resource using the createEmptyCollection() function.
Call the deposit(token) function on the new Collection instance and pass in the borrowed NFT.
The NFT ownership will be transferred to the new Collection instance.

The following functions can be used to read NFT metadata:

* getIDs(): Returns the list of NFT IDs you own.
* borrowNFT(id): Returns a borrowed reference to an NFT by ID.
* borrowAuthNFT(id): Returns an authenticated borrowed reference to an NFT by ID.

The NFT resource defines the following fields:

* id: The unique identifier of the NFT.
* name: The name of the NFT.
* favouriteFood: The favourite food of the NFT.
* luckyNumber: The lucky number of the the NFT

## License
This NFT program is not licensed.
