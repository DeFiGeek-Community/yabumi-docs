# Precondition

## SNS ID

Yabumi uses unique numbers to identify various SNS sites. For example, Discord is ID 1, Twitter is ID 2, etc.. To reduce gas costs, this numbering scheme has been adopted.

## Signatures

The following three components are used for backend signature generation:

1. User ID on the SNS platform (e.g., 123456789).
2. SNS ID (e.g., 1).
3. Minted wallet address (e.g., 0x123456789... - a 40-digit hexadecimal value).

## JointedID

The User ID on the SNS platform and the SNS ID are combined using an underscore, resulting in a JointedID. For example, 123456789\_1.

## Hashing

User ID, JointedID and minted wallet address are concatenated and hashed. This hashed value is used as the signature message.

