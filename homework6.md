# Homework 6 Upside Down Iceberg
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

Read and summarize

## Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router.
Reference: Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router. In USENIX security symposium (jufo level 2). Chapter 3 Design goals and assumptions

Summary Chapter 3 Design goals and assumptions

Main goals: Communications are linked from single user. There are several demands of Tor debloyability for example it has to be cheap to run it and it can't put responsibilities to third parties. Usability is main thing so there are more users and that's how anonymity is guaranteed. In this case usability is a key element of security requirements. The protocol must be flexible and specifications needs to be clear and that includes security parameters also. Tor aims to deploy a simple and stable system that integrates the best accepted approaches to protecting anonymity.
Non-goals: Not peer-to peer because there still are some problems to solve. Not secure to e2e attacks but user can use own onion routers to lower the risk. No protocol normalization. If senders want anonymity from responders while using complex and variable protocols, Tor must be layered with a filtering proxy. By this separation Tor can also provide services that are anonymous to the network yet authenticated to the responder.
Threat-model: The goal is not to prevent traffic confirmation attacks. We aim to prevent traffic analysis attacks, where the adversary uses traffic patterns to learn which points in the network he should attack. 

## Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey.
Reference: Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey. In IEEE Communications Surveys & Tutorials (jufo level 2). 

Summary of Abstract

People are trying to protect their online privacy and it grows popularity of anonymity networks. Tor is most popular network and it protects privacy of the user and services. Also criminals take advantage of anonymity. In this survey has been analyzed known Tor attacks and techniques against anonymisation of users. Survey provides some improvements to Tor network to protect the privacy of the users. 

Summary of I Introduction

Main use of low latency anonymous networks is to provide online privacy security for different kinds of use: private persons in totalitary countries, whistle blowers, military and business organizations with sensitive communications. The most popular service Tor provides anonymity to users and supports the deployment of anonymous services, known as hidden services. But also criminals has taken Tor into use and that's why governments also want to break it's anonymosity. This survey covers about 30 more de-anonymisation attacks than most past surveys. There has been used multi-level taxonomy to categorise de-anonymisation attacks on Tor. In this surveys has been classified and discussed each attack, focusing on the Tor circuit component(s) used and the method of execution. The practicality of those attacks has been analyzed. Finally survey highlights several significant Tor development milestones over the years that are relevant to deanonymisation attacks and discuss how security improvements have made some of the previously possible attacks unfeasible.

Summary of II Background 

Tor uses onion routing. Tor is an overlay network based on Transmission Control Protocol (TCP) that builds circuits from a user to the destination server, which generally consists of three voluntary relays. 
Tor client is an onion proxy (OP). This needs to be installed into users device.
Directory Servers are a small set of trusted and known servers in the network that actively keep details about the status of the complete network. 
Entry Node/Guard is the relay in the Tor network that the client directly connects to. 
Exit Node is the final point it the circuit. Therefore, it knows the IP address of the destination server accessed via the Tor network. This is the last layer of encryption provided by the Tor network. 
The Tor network supports Hidden Services (HS), also known as Onion Services because Tor gives anonymity to user but not to services they use. HS can be hosted on a node inside the Tor network or an external node and these domains ends in .onion.
Introduction Points are random nodes selected by the HS to register its services with the Tor network. The HS then advertises these selected introduction points and its public key in the Hidden Service Directories (HSDirs).
Rendezvous Point (RP) is a random Tor node selected by the client OP before the client initialises a connection with any of the introduction points advertised by the DS. The client selects two other nodes (entry and middle) and establishes a Tor circuit to the RP via these nodes. 
Bridges are normal Tor relays that are not listed publicly in the main Tor directory. They replace guard nodes in the circuit.

Standard Tor Circuit Establishment

Before communicating over the Tor network, a Tor client must establish a circuit through the Tor network. The user is required to have the Onion Proxy (OP) installed on the device being used for browsing. The OP first contacts a DS and requests a list of active relays in the network. Then it selects three relays from the list to act as the entry, middle, and exit nodes, and incrementally creates a circuit by exchanging encryption keys with each node. The key exchange is done via the Diffie–Hellman handshake. Once this connection consisting of three hops has been established, the user can communicate with the intended destination server over the established circuit.

Circuit Establishment for Tor HS

The HS selects multiple introduction points from the available nodes in the Tor network and builds connections to those nodes. Following this, it connects to the DS and advertises a service descriptor with the HS’s public key, expiration time, and the details of the selected introduction points. The HS owner can then advertise the service’s onion address. If users want to access a HS, they need to find its onion address. When the user searches an address in the browser, the OP fetches the service descriptor of that particular HS from the DS. This way, the OP finds out about the HS’s introduction points and its public key. The OP then selects an RP, establishes a Tor circuit to the RP (via two nodes (entry and middle)), and sends a message with the RP’s address, and a one-time secret called the Rendezvous Cookie (RC) to one of the introduction points. The introduction point forwards this message, which is encrypted with the HS’s public key, to the HS. Once the HS receives the message, if it wants to establish a connection with that client, it (HS) selects three Tor nodes (one entry and two middle) and creates a three-hop connection to the RP, which keeps the HS’s identity anonymous from RP. Following this, the client and the HS can communicate using the six-hop circuit via the RP.

Summary of Fig. 6. Taxonomy for Tor attacks (Just the figure on page 2330.)
Taxonomy for Tor Attacks focuses to de-anonymisation attacks. Attacks can be passive or active. They are categorized in 4 different types which can try to exploit 1. side channels, 2. entry and exit routers or 3. onion proxy, onion routers and servers or 4. hybrid attacks. The known attacks are listed in the picture under categories.   

## Halonen, Ollikainen, Rajala 2023: PhishSticks - The Ethical Hackers tool for BadUSB 

Reference: PhishSticks: PhishSticks - The Ethical Hackers tool for BadUSB Watchable: https://www.youtube.com/watch?v=bDzVevtZiWE Watched: 1.12.2024.

Summary: Company's CEO gets an USB stick with a note that in it are the newest payroll information. CEO doesn't follow company's policy and he attaches it to his computer. In this phishstick is keylogger payload but there could be some other USB payload dropper attacks too. When attached to his computer phishstick will use injected keystrokes to open up Windows run and then types a oneliner that fetches the payload via Windows Powershell. This stick records the things CEO does on his computer and by that hacker gets CEO's user credentials. The logged data is stored in the TEMP folder of the victim and sent to the hacker. Phishstick removes the temp data after it has been sent. CEO goes unemployed but there can be quite significant punishments like jail or large monetary losses to company. 

## If you cannot or do not want to do the hands-on darknet tasks, the alternative task is: compare anonymous/pseudonymous networks, such as TOR, I2P, Freenet and others. How do their goals, technology and other features differ? How are they similar? Add references. Link differences and benefits to technical and architecture aspects.

Well I didn't want to do the hands on tasks with Tor so here is my comparison of anonymous networks.

Tor. 

At this homework 6 I have earlier described it's goals and technology. 

I2P.
Reference: Security and Privacy Academy: The Invisible Internet Project (I2P) Explained. Watchable: https://www.youtube.com/watch?v=XT_z7KpXcV0 Watched: 1.12.2024

Dezentralized peer-to-peer anonymous network. The network consists of 50000 devices around the globe. Scattering your traffic. Encrypted access to dark web. E2E encryption using public key cryptography. 
Differences to Tor: Unidirectional tunnels. Incoming and outgoing traffic is separated. Garlic routing. Original messages are divided into smaller messages called cloves. All submessages travels separately through the network to it's destination. It's very hard for hackers to crack the message.
Goals are the same with I2P and Tor.
Plus: every message is e2e encrypted so they are very secured. 
Plus: It uses packet switching and it means high perfomance on network.
Plus: privacy.
Cons: difficult installation and usage (in Tor you just download onion proxy) 
Cons: Users need to be logged in (same with Tor)
Cons: Smaller user base than Tor, attacks are theoretically more likely
Major differencies compared to Tor: I2P is more centralized because of peer-to-peer network. It uses garlic routing (Tor uses only one route). 

Freenet.
Reference: Freenet Project Inc. Websites. 2024. Readable: https://freenet.org/ Read: 1.12.2024. 

Dezentralized peer-to-peer anonymous network. Every peer contributes to a fault-tolerant collective, ensuring services are always available and robust. Every system built on Freenet is fully interoperable by default. The platform’s user-friendly decentralized applications are scalable, interoperable, and secured with cryptography. Freenet is a global key-value store that relies on small world routing for decentralization and scalability. Keys in this key-value store are WebAssembly code. These webassembly keys are also known as contracts, and the values are also known as the contract’s state. Freenet provides a local HTTP proxy that allows data such as a single-page application to be downloaded to a web browser. This application can then connect to the Freenet peer through a websocket connection and through this interact with the Freenet network. Anonymity: While the previous version was designed with a focus on anonymity, the current version does not offer built-in anonymity but allows for a choice of anonymizing systems to be layered on top.

Freenet functions as an end-to-end operating system for decentralized apps. Similar to how you install a web browser once and gain access to applications like Gmail, Facebook, and Reddit without installing additional software, Freenet provides seamless access to a wide range of decentralized applications directly within your browser.

With Freenet, you can discover apps through a decentralized search engine. Obtain apps through Freenet. Use apps entirely on Freenet. Additionally, you don’t have to use Freenet through a browser. The “Freenet core” is small (<10MB) and can be easily embedded in other software, which can then communicate with the Freenet core over an HTTP/WebSocket API.

Goals: Freenet is a complete solution. Freenet functions as an end-to-end operating system for decentralized apps.

Comparison:

Similarities: all are anonymous dezentralized networks. All use cryptography as a key element in the solution.
Differencies: all of them work technically/architecturally in a different way. I2P and Freenet are peer-2-peer solutions while Tor's communications are linked to single user. Tor has widest userbase. I2P lacks usability. Tor gives anonymity to user but not to services they use. Before communicating over the Tor network, a Tor client must establish a circuit through the Tor network only through one route. In I2P original messages are divided into smaller messages called cloves. Freenet functions as an end-to-end operating system for decentralized apps. 

## c) Onion. In your own words, how does anonymity work in TOR? (e.g. how does it use: public keys, encryption, what algorithms? 

First user starts Tor client (onion proxy/OP) and then client starts to create the circuit with three nodes. The OP creates a circuit by exchanging encryption keys with each node. The key exchange is done with the Diffie–Hellman handshake. The OP starts to create first part of circuit by giving negotiaded key to node 1 using RSA encryption. First node returns negotiaded key with secure hash function. Then OP creates the second part of the circuit and returns information gotten from first node through that node to reach second node. New negotiaded key with it's hash functions are returned through first node to OP. Then OP starts to create the last node of the circuit. It returns the information gotten from second node through nodes 1 and 2 to node 3 which returns third negotiaded key with secure hash function through nodes 2 and 1 to onion proxy. Now there is secure anonymous network created.

Reference: Reference: Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey. In IEEE Communications Surveys & Tutorials Fig. 3. Tor circuit creation and data transmission. Readable: https://ieeexplore.ieee.org/ielx7/9739/9621320/09471821.pdf Read: 4.12.2024

## d) What kind of the threat models could TOR fit? 

A global passive adversary
Traffic confirmation attacks
Traffic analysis attacks

Reference: Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router. Chapter 3.1 Threat model Readable: https://css.csail.mit.edu/6.858/2022/readings/tor-design.pdf Read: 4.12.2024

## e) Don't stick that stick. How does PhishSticks attack work? Would a typical organization be vulnerable? Does this link to a broader category of attacks and defenses? How could the risk be mitigated?

As we are humans, it's easy to get someone attach unknown USB stick to their machine, because people are kind and could think that maybe some coworker has forgotten their USB stick. People want to open it that they could know who's it is and return it. So people are the vulnerability here like in many other attack cases of phishing. It goes with the content of social engineering by attackers. Risk can be mitigated by educating workers in general on phishing attacks and more specifically never attach USB sticks on computer. Those should be given to service desk who can safely check it if necessary.
