# Mint NFT

## 1. Requirements for Minting Yabumi NFT&#x20;

When minting Yabumi NFT, the contract receives the following data from the frontend:

* JointedID
* Signature (r)
* Signature (s)
* Signature (v)

## 2. Creation of Signature Data

Using the following data, the contract generates signature data:

* JointedID
* Minting address (msg.sender)

## 3. Verification of Signature Address

Using the following data, the contract verifies the backend signature address:

* Signature data created in step 2
* Signature (r)
* Signature (s)
* Signature (v)

## 4. Address Error Handling

It returns an error if the following two data do not match:

* Backend signature address verified in step 3
* Minting address

## 5. Minting Error Handling

If NFT has minted from the JointedID, an error is returned.

## 6. Index Assignment

The contract assigns a special tokenID if steps 4 and 5's checks are successful.

## 7. Saving the Jointed ID

To avoid minting the same ID more than once, the JointedID is saved as a minted ID in a variable.

## 8. Linking with Token ID

The contract stores the JointedID and Token ID linkage information in a variable.

## 9. Saving the Minting Wallet Address

The contract stores the wallet address link to the Token ID in a variable, making it possible to retrieve the wallet address from the Yabumi NFT Token ID.

## 10. Minting Procedure

Using the allocated Token ID and the wallet address, the contract carries out the minting.

## 11.Minting Event Emission

Store the JointedID and TokenID and trigger the emit event
