# h5 HelSec
x) Watch and summarize. Add your own comments, ideas and questions.
Two full length HelSec presentations on the November event (2024-11-21 w47 Thu)
Voluntary bonus: A third one.
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

Reference: HelSec November meetup Twitch stream 21.11.2024 18.15-21.

## 1.	Speaker: Jos Helmich: Industrial cybersecurity

EU agency for cybersecurity has a new advisor group Enisa. General EU Laws & Directives: GDPR, demands that privacy is respected. Compared to EU legislation, US is far behind.
New cybersecurity laws are coming. NIS-2 in manufacturing has enterprise level standards (level4-5) for confidentiality, integrity and availability. Also there is manufacturing level controls from level 0 to level 3 for availability, integrity and confidentiality. NIS-2 is about following instructions of cybersecurity in EU level. It includes risk management standards and reporting of deviation. CRA (cybersecurity resilience act) has been published this week and it applies to digital products that can be attached to network or other device. Your company is responsible of for whom you buy stuff and that in manufacturing of those stuff has been followed good cybersecurity standards.  Act 62443 has some standards for secure software development like system and component requirements. When you sell cybersecurity services or products you need to follow this law. Also Artificial Intellicence Act is coming and there is product safety requirements, data requirements (GDPR) and CRA. 

Own comments: It’s good to know that in EU we are protecting privacy but what can we do when big tech countries like China, America and Russia don’t follow this regulation. You have to be very well knowledged in tech stuff that you know the risks and can try to minimize those. 

## 2.	Speaker: Heikki Juva: State of Union

Juva has done RED (radio equipment directive) and CRA testing in practice. Regulation RED has 3 important points: network security, protecting personal information of the user and financial misuse. 
CRA has 2 important points on Annex 1: Technical security requirements and vulnerability handling requirements. Laws are being enforced and Heikki thinks about CRA that technical security and vulnerability reporting is coming.

Findings of Heikki’s testing. Research questions were: How do consumer devices communicate? To where? Why? Testing was done with 10 most popular consumer devices that are connected to Internet.

RED Device classification: If device is connected to network then RED part 1 requirements apply. If device collects personal data (includes smart toys and childcare equipments) then RED part 2 requirements apply. If device handles financial assets like money or cryptocurrency then RED part 3 requirements apply. 

Some promising requirements: companies have to report vulnerabilities, validate input in all interfaces, follow cryptography best practices about protection of security and network assets, good password management and content filtering is in place if device is a smart toy.
Some problematic requirements: less secure solutions are accepted, if external devices ensure security, then all security measures are not needed, and also evaluation can be paper-based.
One example was Case Eagle: two products: IP camera and o2 meter and heartrate monitor. 
RED part 1 case eagle: only software updates were enforced but device storage was not secure and there were tens of vulnerabilities including password. 
RED part 2: privacy. Case Eagle: GDPR was bypassed. Only sensors that could affect user’s privacy were documented but otherwise privacy was not protected at all. 

Statistics of overall testing: most of the data was encrypted. Most common issues were that data was not removed, privacy information was shared with 3rd parties and track record of how devices work is not known by seller. 

So overall Heikki has created a practical way to study does equipments, that goes to network, follow the standards of the new laws. 

Own comments: I really like this practical way to simplify law to users. Even I could check the most important things about product security and privacy by following these questions. 

## 3.	Speaker: Joona Immonen: My experiences on Defender External Attack Surface Management (EASM)

What is EASM and why should I care? It isn’t official MS tool yet. It’s meant for brand and infrastructure exposure, threat hunting, penetration testing, vulnerability management and risk assessment.
EASM Features: continuous discovery of digital attack surface and gives external view of your infrastructure. 3/5 phases of penetration test: reconnaissance, scanning and enumeration. It helps you to identify digital resources that are accessible from internet. 
Experiences: It basically gives you an inventory. You can look dasboards of your threats. All functionalities are not working fully. Pricing is unclear but you can use 30 days trial for free. You don’t have visibility what the tool actually does. 

There is also open source EASM tool Owasp Amass. This tool isn’t perfect either but it’s efficient and didn’t require that much.

Tools gave different results and findings.

Own comments: It is odd that products for same purpose will give you totally different results.

