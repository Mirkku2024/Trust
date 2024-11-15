## h4 To the moon!
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

# Summarize Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System

1 Introduction
There are some weaknesses when using trusted third parties to accept electronic transactions for example extra costs for transactions and limiting minimun transaction size. Still processes are not fraudless. When system is based on cryptographic proof any two parties can make transactions between each other and avoid weaknesses that are build in current systems using only financial institutions as trusted third parties. Cryptographic proof is made when distributed timestamp server is in use to generate computational proof of the chronological order of transactions.

2 Transactions
In this system an electronic coin is a chain of digital signatures. Each owner transfers the coin to the next by digitally signing a hash of the previous transaction and the public key of the next owner and adding these to the end of the coin. A payee can verify the signatures to verify the chain of ownership.

3 Timestamp Server
Solution starts from a timestamp server. It takes a hash of a block of items to be timestamped and publishes it. Each timestamp includes the previous timestamp in
its hash and those are a chain, with each additional timestamp reinforcing the ones before it. 

4 Proof-of-Work
The proof-of-work involves scanning for a value that when hashed, such as with SHA-256, the hash begins with a number of zeros. The block is incrementing a nonce in the block until a value is found that gives the block's hash the required zero bits.  

5 Network
The steps to run the network are: New transactions are send to all nodes. Each node collects new transactions into a block. Each node creates a secured hash which begins with zeros for its block. ) When a node finds a proof-of-work, it broadcasts the block to all nodes.
5) Nodes accept the block only if all transactions in it are valid and not already spent.
6) Nodes express their acceptance of the block by working on creating the next block in the
chain, using the hash of the accepted block as the previous hash

6 Incentive



Reference: Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System (A colored HTML version) Readable: https://bitcoin.org/bitcoin.pdf Read: 15.11.2024
