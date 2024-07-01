### [S-#]
storing data on-chain makes it visible for everyone.

**Description:** 
The data stored on the blockchain is visible to everyone. The `PasswordStore:s_password` is intended to be accessible only through `PasswordStore::getPassword` function but in can be derived directly from blockchain. 

**Impact:**
anyone can read the password and breake the security of passwords in the protocol. 

**Proof of Concept:**

**Recommended Mitigation:** 

you can encrypt the passwords on-chain and then after read, decrypt it.
also you don't need view functions because public variables can be read without functions.