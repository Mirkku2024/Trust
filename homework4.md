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

# Other subtasks

a) Wallet. Create a BitCoin testnet wallet. (For example, electrum)
Electrum installed.
![image](https://github.com/user-attachments/assets/58d51fee-e6ab-4e53-a448-9a1883de129d)
![image](https://github.com/user-attachments/assets/d810a34a-14ab-4adb-a188-8a1264e3a9d1)
![image](https://github.com/user-attachments/assets/56f1c4e8-706b-4af9-a978-ab93cfd26e3b)
![image](https://github.com/user-attachments/assets/2b651a73-892b-4f84-be44-74bc99d616c0)
![image](https://github.com/user-attachments/assets/7a8870ab-05ab-49e3-8eb7-50dc2949f61e)
Wallet created
![image](https://github.com/user-attachments/assets/b6a46de8-4116-470d-bdbf-d805dce7ec1d)

b) Faucet. Get worthless fake money from a testnet Bitcoin faucet.
First and second try didn't get me in. 

![image](https://github.com/user-attachments/assets/4a03cba9-dc4d-4631-8cf0-2593d6a2252c)

I opened another test faucet.

![image](https://github.com/user-attachments/assets/49e29068-4bec-4488-9aff-f97329c6d64e)

![image](https://github.com/user-attachments/assets/c08a5cee-126e-4d8a-bf56-643b2c3d1a70)

I tried to use an receiving address from Electrum but got an notification. At this point I stopped trying.

![image](https://github.com/user-attachments/assets/0f55ac35-d95d-4002-a1e7-6a2ad69fd0d0)

c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 73.
Couldn't do this because I don't understand what to do.

d) Recycle. Move the testnet money back to the same faucet you got it from.
Couldn't do this because I don't understand what to do.

e) Explorer. Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions.

![image](https://github.com/user-attachments/assets/5fda4b07-17d1-49b5-ab8d-5675be72f23e)

![image](https://github.com/user-attachments/assets/1a35160b-6dda-468c-a55e-d2098a9f66bd)

![image](https://github.com/user-attachments/assets/46708503-9150-428a-ac58-185d994abeef)

![image](https://github.com/user-attachments/assets/b1f22fbc-5abe-4760-be77-ee1738e6634a)

![image](https://github.com/user-attachments/assets/f62a050a-6ebd-4d7f-8dec-f4aa0ce270af)

![image](https://github.com/user-attachments/assets/31ed63d0-9371-439c-a177-cf530d8219fc)


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
