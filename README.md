# Trust
Homework reports for security course taught by Tero Karvinen

# First homework
## Summary from Cyber kill chain
Traditional way of defensing network isn't enough anymore. With kill chain model you can gain better understanding of threats. This mitigates risks and vulnerabilities when hackers are targeting your company. There are 7 different phases in kill chain: reconnaissance, weaponization, delivery, exploitation, installation, C2 and actions. You must analyze all attacks and build defense towards them so they wouldn't happen in the future. Also with the knowledge of failed intrusions you can guess attackers next attempt and defend your network against those.
Own comment: I didn't search how old is this whitepaper. I understand the benefit of this approach but it feels very heavy user tool and needs resources. Is there a way to make this kind of stuff in smaller companies?

Reference: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains by Eric M. Hutchins, Michael J. Cloppert, Rohan M. Amin - Lockheed Martin Corporation read from https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf on 28.10.2024.

## Summary from Darknet diaries Episode 127 Maddie
Maddie Stone is a security researcher for Google’s Project Zero. In this episode we hear what it’s like battling zero day vulnerabilities. Her career started there as working as a reverse-engineer trying to detect malwares from Android code and telling developers how to solve them. One case named Chamoi was a bottnet using very sofisticated native library in an app on android devices. This case took over a year to be solved out. That case lead Maddie to start working on Project Zero. Project Zero team tries to find unknown malwares and Maddie's knowledge brought a new aspect to this work as finding patterns between unknown malwares. Maddie has gained a lot of respect due to her work but also personal threats for being a target for large criminal organizations and even nation's army. Maddie thinks that the work Project Zero does makes it lots harder for hackers to create new types of malware. 
Own comment: Maddie is doing very interesting job. In the episode was lots of discussion of the attackers nature that are those real criminals trying to make out some money or government's own armies attacking other states. Unfortunately this is modern warfare and I guess it's a lot cheaper and easier than using real weapons.

Reference: https://darknetdiaries.com/episode/127/

## Att&ck Enterprise Matrix
Explanation of tactic: it's a reason what attacker wants to gain by hacking. It answers why hacker is doing this.
Example Reconnaissance, getting information for future operations

Explanation of technique: it's a technique what attacker is using in hacking. It answers how hacker is doing this.
Example Gather victim identity information

Explanation of procedure: it describes the way attacker is using different techniques to gain his/her goals. 
Example Magic hound: Magic Hound has compromised personal email accounts through the use of legitimate credentials and gathered additional victim information

Reference: https://attack.mitre.org/resources/faq/ 
https://attack.mitre.org/matrices/enterprise/

## Comparing Cyber Kill Chain and ATT&CK Enterprise matrix 
There are similarities in both models. Both try to first understand why level and then there are more specified ways to defend company from different types of attacking techniques. ATT&CK is more comprehensive and detailed model. It could be used in security service providers. Cyber Kill Chain supports risk management and investing into security things. It's easier to apply when company's security personnel are planning how to build and maintain good security infrastructure. I think these could be used in midsize or larger companies. Especially ATT&CK is for very large companies who has their own security departments for implementing it.

## Security incident example
My example is TietoEvry's resent ransomware case. This is direct copying as a summary from their press release. One of Tietoevry’s datacenters in Sweden was subject to a ransomware attack during the night of January 19-20.2024. Tietoevry’s monitoring detected the suspicious and unusual activity and Tietoevry was able to stop the attack, limiting its impact to one platform. However, the attack unfortunately impacted several Tietoevry’s customers’ services across industries and has thus been visible in the Swedish society in many ways. Tietoevry initiated the restoration of affected customer services with the highest priority and was able to restore majority of the affected servers in a systematic manner during the first days after the attack, enabling several customers to have their services operational from this stage. However, due to relatively many customer-specific solutions within the affected platform, there have been varying degrees of impact and consequently varying recovery processes. With the exception of efforts continuing with few customers, all other impacted customer services were fully restored by mid-March. Tietoevry’s security experts started to assess the potential attack vectors immediately, including a large-scale data analysis. Our analysis concluded the most probable path used by the attacker to gain unauthorized access to the datacenter. As immediate action from the ransomware attack, Tietoevry has intensified the surveillance of its infrastructure. In light of Tietoevry’s role as a service provider, the criminal nature of the attack and for security reasons, Tietoevry cannot publicly share technical details of the attack. Tietoevry has maintained an active dialogue with the authorities since the attack took place and has shared the findings with them. Tietoevry is at all times committed to respecting contractual obligations and customer confidentiality, thus the company cannot share customer-specific information regarding this case.

So conclusion based on press release summary is that attacker gained access to datacenter and could take control of the servers. Besides the service breaks from couple of days to couple of months, I guess TietoEvry has paid a lot of money to customers for this security breach and SLA's. Business impacts for TietoEvry's customers and their customers has not been told but it's been quite on impact. And story doesn't tell if they have had to pay ransomware about the customers whose services they couln't restore from TietoEvry's side.

Reference: https://www.tietoevry.com/en/newsroom/all-news-and-releases/press-releases/2024/04/tietoevry-conclusions-on-the-ransomware-attack/

## Install Debian on Virtualbox
Report your work, including the environment (including host OS, the real physical computer used), the steps you took and their results.

Own computer: Windows 10 Pro, Intel Core i3 10100 CPU 3,6 GHz, 64-bit operating system

![image](https://github.com/user-attachments/assets/9a05da3e-0ba3-4f52-8d7e-9ac5835db497)

![image](https://github.com/user-attachments/assets/fcd4841d-dd5e-4950-9b09-5d3138f68a8b)

![image](https://github.com/user-attachments/assets/3a633cb6-9e7f-464b-bca5-d9485f588682)

![image](https://github.com/user-attachments/assets/08f9bea9-ff9b-49e8-a968-bf3707429ce1)

![image](https://github.com/user-attachments/assets/284336fe-46bc-4233-8f1f-d48d1c83db8a)

![image](https://github.com/user-attachments/assets/364b73f9-cfb0-4f1a-9dd1-7b0e3d65b7a0)

![image](https://github.com/user-attachments/assets/210fcc8b-3b75-4b57-9927-ecd087855450)

![image](https://github.com/user-attachments/assets/fe7fe8c5-fcbd-416a-901c-bc10d026defa)

![image](https://github.com/user-attachments/assets/a56b3265-fd82-491c-b4e1-725c60148ee0)

![image](https://github.com/user-attachments/assets/d6e408d6-b933-4a42-8114-be8082dd9407)
















