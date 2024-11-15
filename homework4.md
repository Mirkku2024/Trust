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
The steps to run the network are: new transactions are send to all nodes. Each node collects new transactions into a block. After that those nodes create a secured hash which begins with zeros for it' block. When a node finds a proof-of-work, it broadcasts the block to all nodes. Blocks are accepted if all transactions in it are valid and not already spent. Then nodes express their acceptance of the block by creating the next block in the chain, using the hash of the accepted block as the previous hash.

6 Incentive
The first transaction in a block is a special transaction that starts a new coin owned by the creator of the block. This adds an incentive for nodes to support the network, and provides a way to initially distribute coins into circulation.

Reference: Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System (A colored HTML version) Readable: https://bitcoin.org/bitcoin.pdf Read: 15.11.2024

a) Wallet. Create a BitCoin testnet wallet. (For example, electrum)

b) Faucet. Get worthless fake money from a testnet Bitcoin faucet.

c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 73.

d) Recycle. Move the testnet money back to the same faucet you got it from.

e) Explorer. Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions.

f) RogeCoin. Critically comment on Honest Ads: If Cryptocurrency Was Honest 
Identify and list arguments made. Provide commentary to support and challenge each of the claims. If you can, provide references or real life examples to your claims. 

Argument 1 Cryptocurrency is easier to lose than real money
+ Actually it doesn't collapse when government collapses
+ When using trustworthy providers it's reliable
+ Cryptocurrencies are in hype and it has gained value
- You can get scammed unless you don't carefully choose reliable provider Reference: https://www.investopedia.com/biggest-mistakes-crypto-investors-make-8712112
- It's value can be gone if it gets negative publicity

Argument 2 Cryptocurrency is far more volatile
+/- Cryptocurrency is dezentralized Reference: https://www.investopedia.com/terms/c/cryptocurrency.asp
- 

Argument 3 Cryptocurrency slaughters the environment
- Uses more electricity than Switzerland Reference: https://unu.edu/press-release/un-study-reveals-hidden-environmental-impacts-bitcoin-carbon-not-only-harmful-product
- Cryptocurrency mining will raise your costs hugely
- 
Argument 4 Cryptocurrency can't be exchanged for vast majority of goods and services
+ Fungibility
- You can exchange it for criminal stuff
  
Argument 5 Cryptocurrency will make you look sexy in the age of consent laws.
+
- Cryptocurrency has been used for money laundering Reference: https://baselgovernance.org/publications/quick-guide-1-cryptocurrencies-and-money-laundering-investigations
- 
Argument 6 If you don't know about blockchain you can lose a large amount of real money.
+ 
- What happens if you forgot your electronic wallets password? Reference: https://www.investopedia.com/biggest-mistakes-crypto-investors-make-8712112
  
Argument 7 Cryptocurrency will remain it's value as long as Cryptofirms keep talkin' about it and internet is up and running
+
- You just invest more and more but it loses value
  
Argument 8 Almost 90 % of cryptocurrencies are already mined 
- You need a lot of CPU to mine just a couple of coins Reference: https://www.newsbtc.com/news/how-long-it-will-take-to-mine-bitcoin/

Reference: Honest Ads: If Cryptocurrency Was Honest. Video. Watchable: https://www.youtube.com/watch?v=GUs5y9leCyA Watched: 15.11.2024.
