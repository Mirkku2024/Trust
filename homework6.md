# Homework 6 Upside Down Iceberg
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

Read and summarize (briefly, e.g. with some bullets)

## Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router.
Reference: Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router. In USENIX security symposium (jufo level 2). Chapter:
3 Design goals and assumptions

Summary Chapter: 3 Design goals and assumptions

Main goals: Communications are linked from single user. There are several demands of Tor debloyability for example it has to be cheap to run it and it can't put responsibilities to third parties. Usability is main thing so there are more users and that's how anonymity is guaranteed. In this case usability is a key element of security requirements. The protocol must be flexible and specifications needs to be clear and that includes security parameters also. Tor aims to deploy a simple and stable system that integrates the best accepted approaches to protecting anonymity.
Non-goals: Not peer-to peer because there still are some problems to solve. Not secure to e2e attacks but user can use own onion routers to lower the risk. No protocol normalization. If senders want anonymity from responders while using complex and variable protocols, Tor must be layered with a filtering proxy. By this separation Tor can also provide services that are anonymous to the network yet authenticated to the responder.
Threat-model: The goal is not to prevent traffic confirmation attacks. We aim to prevent traffic analysis attacks, where the adversary uses traffic patterns to learn which points in the network he should attack. 

## Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey.
Reference: Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey. In IEEE Communications Surveys & Tutorials (jufo level 2). 

Summary of Abstract

People are trying to protect their online privacy and it grows popularity of anonymity networks. Tor is most popular network and it protects privacy of the user and services. Also criminals take advantage of anonymity. In this survey has been analyzed known Tor attacks and techniques against anonymisation of users. Survey provides some improvements to Tor network to protect the privacy of the users. 

Summary of I Introduction

Main use of low latency anonymous networks is to provide online privacy security for different kinds of use: private persons in totalitary countries, whistle blowers, military and business organizations with sensitive communications. The most popular service Tor provides anonymity to users and supports the deployment of anonymous services, known as hidden services. But also criminals has taken Tor into use and that's why governments also want to break it's anonymosity. This survey covers about 30 more de-anonymisation attacks than most past surveys. There has been used multi-level taxonomy to categorise de-anonymisation attacks on Tor. In this surveys has been classified and discussed each attack, focusing on the Tor circuit component(s) used and the method of execution. The practicality of those attacks has been analyzed. Finally survey highlights several significant Tor development milestones over the years that are relevant to deanonymisation attacks and discuss how security improvements
have made some of the previously possible attacks unfeasible.

Summary of II Background (to the end of "B. Circuit Establishent for Tor HS")

Tor uses onion routing. Tor is an overlay network based on Transmission Control Protocol (TCP) that builds circuits from a user to the destination server, which generally consists of three voluntary relays. 
Tor client is an onion proxy (OP). This needs to be installed into users device.
Directory Servers are a small set of trusted and known servers in the network that actively keep details about the status of the complete network. 
Entry Node/Guard is the relay in the Tor network that the client directly connects to. 
Exit Node is the final point it the circuit. Therefore, it knows the IP address of the destination server accessed via the Tor network. This is the last layer of encryption provided by the Tor network. 
The Tor network supports Hidden Services (HS), also known as Onion Services because Tor gives anonymity to user but not to services they use. HS can be hosted on a
node inside the Tor network or an external node and these domains ends in .onion.
Introduction Points are random nodes selected by the HS to register its services with the Tor network. The HS then advertises these selected introduction points and its public key in the Hidden Service Directories (HSDirs).
Rendezvous Point (RP) is a random Tor node selected by the client OP before the client initialises a connection with any of the introduction points advertised by the DS. The client selects two other nodes (entry and middle) and establishes a Tor circuit to the RP via these nodes. 
Bridges are normal Tor relays that are not listed publicly in the main Tor directory. They replace guard nodes in the circuit.

Standard Tor Circuit Establishment

Before communicating over the Tor network, a Tor client must establish a circuit through the Tor network. The user is required to have the Onion Proxy (OP) installed on the
device being used for browsing. The OP first contacts a DS and requests a list of active relays in the network. Then it selects three relays from the list to act as the entry, middle, and exit nodes, and incrementally creates a circuit by exchanging encryption keys with each node. The key exchange is done via the Diffie–Hellman handshake. Once this connection consisting of three hops has been established, the user can communicate with the intended destination server over the established circuit.

Circuit Establishment for Tor HS

The HS selects multiple introduction points from the available nodes in the Tor network and builds connections to those nodes. Following this, it connects to the DS and advertises a service descriptor with the HS’s public key, expiration time, and the details of the selected introduction points. The HS owner can then advertise the service’s onion address. If users want to access a HS, they need to find its onion address. When the user searches an address in the browser, the OP fetches the service descriptor of that particular HS from the DS. This way, the OP finds out about the HS’s introduction points and its public key. The OP then selects an RP, establishes a Tor circuit to the RP (via two nodes (entry and middle)), and sends a message with the RP’s address, and a one-time secret called the Rendezvous Cookie (RC) to one of the introduction points. The introduction point forwards this message, which is encrypted with the HS’s public key, to the HS. Once the HS receives the message, if it wants to establish a connection with that client, it (HS) selects three Tor nodes (one entry and two middle) and creates a three-hop connection to the RP, which keeps the HS’s identity anonymous from RP. Following this, the client and the HS can communicate using the six-hop circuit via the RP.

Summary of Fig. 6. Taxonomy for Tor attacks (Just the figure on page 2330.)
Taxonomy for Tor Attacks focuses to de-anonymisation attacks. Attacks can be passive or active. They are categorized in 4 different types which can try to exploit 1. side channels, 2. entry and exit routers or 3. onion proxy, onion routers and servers or 4. hybrid attacks. The known attacks are listed in the picture under categories.   


Halonen, Ollikainen, Rajala 2023: PhishSticks - The Ethical Hackers tool for BadUSB (Video, about 3 minutes)

If you cannot or do not want to do the hands-on darknet tasks, the alternative task is: based on literature only (no hands on tests, no installation), compare anonymous/pseudonymous networks, such as TOR, I2P, Freenet and others. How do their goals, technology and other features differ? How are they similar? Add references. Link differences and benefits to technical and architecture aspects.

c) Onion. In your own words, how does anonymity work in TOR? (e.g. how does it use: public keys, encryption, what algorithms? This subtask does not require tests with a computer.)
d) What kind of the threat models could TOR fit? (This subtask does not require tests with a computer.)
e) Don't stick that stick. How does PhishSticks attack work? Would a typical organization be vulnerable? Does this link to a broader category of attacks and defenses? How could the risk be mitigated? (This subtask does not require tests with a computer.) (If you want, you can view PhishSticks on Github and PhishSticks Youtube channel.
