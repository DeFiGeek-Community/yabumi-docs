# Burn NFT

## 1. Inputs&#x20;

The frontend sends the Token ID as a parameter to the contract.

## 2. Address Error Handling&#x20;

If any address other than below tries to carry out the burn, it returns an error.

* The address that owns the Token ID received as a parameter
* The minting address corresponding to the Token ID

## 3. Initialization

The contract initializes recorded variables if the check from step 2 is successful.

## 4. Burn

The contract executes the burning process for the specific Token ID Yabumi NFT.
