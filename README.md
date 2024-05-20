# my-etherjs-notes

## Some Common Terminology
To begin, it is useful to have a basic understanding of the types of objects available and what they are responsible for, at a high level.

### Provider
A Provider is a read-only connection to the blockchain, which allows querying the blockchain state, such as account, block or transaction details, querying event logs or evaluating read-only code using call.

If you are coming from Web3.js, you are used to a Provider offering both read and write access. In Ethers, all write operations are further abstracted into another Object, the Signer.

### Signer
A Signer wraps all operations that interact with an account. An account generally has a private key located somewhere, which can be used to sign a variety of types of payloads.

The private key may be located in memory (using a Wallet) or protected via some IPC layer, such as MetaMask which proxies interaction from a website to a browser plug-in, which keeps the private key out of the reach of the website and only permits interaction after requesting permission from the user and receiving authorization.

### Transaction
To make any state changes to the blockchain, a transaction is required, which requires a fee to be paid, where the fee covers the associated costs with executing the transaction (such as reading the disk and performing maths) and storing the updated information.

If a transaction reverts, a fee must still be paid, since the validator still had to expend resources to try running the transaction to determine that it reverted and the details of its failure are still be recorded.

Transactions include sending ether from one user to another, deploying a Contract or executing a state-changing operation against a Contract.

### Contract
A Contract is a program that has been deployed to the blockchain, which includes some code and has allocated storage which it can read from and write to.

It may be read from when it is connected to a Provider or state-changing operations can be called when connected to a Signer.

### Receipt
Once a Transaction has been submitted to the blockchain, it is placed in the memory pool (mempool) until a validator decides to include it.

A transaction's changes are only made once it has been included in the blockchain, at which time a receipt is available, which includes details about the transaction, such as which block it was included in, the actual fee paid, gas used, all the events that it emitted and whether it was successful or reverted.
