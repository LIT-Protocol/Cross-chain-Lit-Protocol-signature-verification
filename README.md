Write a smart contract to perform Lit Protocol signature verification on Celo (or any EVM Chain that supports a pre-compile for BLS12-381 (EIP-2537))

There are a handful of blockchains that already support a pre-compile for BLS12-381, like Celo. For this bounty, pick a popular blockchain that supports this pre-compile and write the smart contract to verify the network signature created by Lit Protocol. This will enable developers on chains to verify data about token holdings across blockchains.  Please document your code and architecture decisions, and any areas where gas / efficiency improvements could be made.  Also, we are aware that a signed JWT is not efficient to verify in Solidity, so please tell us the most efficient way to deliver signed data and a signature and we will modify the Lit Protocol to return data in this format in the future.

### Submission Requirements
A working connection between two chains with a demo video with documentation.
### Judging Criteria
This submission will be judged on usability and completeness. For example, if other people and use this connection after the hackathon, that's most favorable. 
### Winner Announcement Date
12/20/21
### Resources
https://developer.litprotocol.com/docs/intro/ + https://litgateway.com/discord (Discord)

To easily obtain a signature from the Lit Protocol, you can follow these instructions: https://github.com/LIT-Protocol/lit-js-sdk#signed-chain-data---cross-chain-communication-and-authentication-without-provisioning-access-beforehand

Note that the thing being signed is a JWT, which is base64 encoded JSON.  To verify this in solidity, you will likely need to parse the JWT and pass in the components (header, payload, signature) separately.  
