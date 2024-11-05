# Trust
Homework reports for security course taught by Tero Karvinen

# Second homework Pubkey 
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

# Summary from  Schneier 2015: Applied Cryptography: Chapter 2 - Protocol Building Blocks
2.5 Communications Using Public-Key Cryptography
Whitfield and Hellman invented public-key cryptography in 1976. They used two different keys, the other one was public and the other private. The point is that you can encrypt a message with a public key but it can only opened with certain private key. Example is that Alice sends a message to Bob which she has encrypted with Bob's public key. Bob opens it with using his own private key.

2.6 Digital Signatures
Ralph Merkle invented digital signature trees which is a basis nowadays. It's faster to sign documents with Public-Key Cryptography and One-Way Hash Functions. In practise Alice makes a one-way hash of a document. Then se encrypts the hash with her private key. Then the document is signed. Alice sends the document and the signed hash to Bob. Then Bob makes a one-way hash of the document that Alice sent. Next Bob is using the digital signature algorithm and decrypts the signed hash with Alice's public key. If the signed hash matches the hash he generated, the signature is valid. Using timestamps you can avoid cheating.

2.7 Digital Signatures With Encryption
When digital signatures are combined with public-key cryptography, we have the security of encryption and the authenticity of digital signatures. For security you should have two pairs of keys, one for signing and one for encrypting messages. Also timespams are needed.

2.8 Random And Pseudo-Random-Sequence Generation
"Pseudo-random sequence is one that looks random. The sequence's period should be long enough so that a finite sequence of reasonable length—that is, one that is actually used—is not periodic. For a sequence to be cryptographically secure pseudo-random, it must also be unpredictable. It must be computationally infeasible to predict what the next random bit will be, given complete knowledge of the algorithm or hardware generating the sequence and all of the previous bits in the stream. A sequence generator is real random if it has this additional third property: It cannot be reliably reproduced. If you run the sequence generator twice with the exact same input, you will get two completely unrelated random sequences. The output of a generator satisfying these three properties will be good enough for a one-time pad, key generation, and any other cryptographic applications that require a truly random sequence generator."

Reference: Schneier, P. Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition. 2015. Wiley. Readable: https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/ Read: 2.11.2024

## Summary of Rosenbaum 2019: Grokking Bitcoin Chapter 2. Cryptographic hash functions and digital signatures / Digital signatures
Digital signature can be compared to real one. Typical use of digital signatures are that when you send other people some digital material, he or she can trust it's the original content by verifying it with senders public key. You can use a random number generator  to create a private key. That generator is available on almost all operating systems. Then you can transform the private key into a public key using a public-key derivation function. Public-key derivation is a one-way function, you can’t derive the private key from the public key. Keys are used to encrypt and decrypt data. When you see the little padlock in the address bar of your web browser, then you know that before mentioned are in use to secure your communication. With signature you can use hashes. Then you can authenticate it. Both parties need to use the exact same digital signature scheme. This must be agreed on beforehand, but it’s usually standardized. It's important to ensure that your own private key is in a safe place and no one else can access it. Otherwise you can be fraud. 

Reference: Rosenbaum, K. Grokking Bitcoin. 2019. Manning Publications. New York. Readable: https://learning.oreilly.com/library/view/grokking-bitcoin/9781617294648/ Read: 2.11.2024

## Other subtasks from lesson 2
a) Pubkey today. 
Today I have used public key cryptography when I used mobile banking services, email and also with WhatsApp messages and when I sign into some apps on my mobilephone and it uses mobilephones password management. 

Banking services: Couln't find relevant information from Nordea website. When I go into app it takes facial recognition. 

Email: There are several steps in email services that provide security. "SPF uses a TXT record in DNS to identify valid sources of mail from the MAIL FROM domain, and what to do if the destination email server receives mail from an undefined source. DKIM uses a domain to digitally sign important elements of the message (including the From address) and stores the signature in the message header. The destination server verifies that the signed elements of the message weren't altered. DMARC uses SPF and DKIM to check for alignment between the domains in the MAIL FROM and From addresses. DMARC also specifies the action that the destination email system should take on messages that fail DMARC, and identifies where to send DMARC results (both pass and fail)."
Reference: https://learn.microsoft.com/en-us/defender-office-365/email-authentication-about

WhatsApp: Your conversation are private. Full encryption retains personal messages between you and people you have chosen. Even WhatsApp can't read those. Couln't find more detailed information from WhatsAPP guides.
Reference: Information in WhatsApp

Password management: "A passkey eliminates the need for a password by using a unique digital key that only works from the site or app it was created for, so you don’t have to worry about website leaks or phishing. Passkeys are securely synced across Apple devices. Just use Touch ID or Face ID to authenticate and you’re done."
Reference: https://www.apple.com/privacy/

b) Messaging. Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. Don't use Tero as a name of any party, unless that's your given name.)
Unfortunately I could't do this since the Linux Debian virtual machine doesn't work on my computer. I progressed with this when using another computer but Debian doesn't accept my password. I reseted Debian and made it again but still same problems occure and trying to google solutions didn't help. 
Reference: https://terokarvinen.com/2023/pgp-encrypt-sign-verify/

c) Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen. 

I'll try to encrypt an Outlook message. Microsoft advices this: 

![image](https://github.com/user-attachments/assets/b32b30cb-7d96-41ba-bf85-520f190092a8)

Reference: https://support.microsoft.com/en-us/office/send-encrypted-email-messages-in-outlook-for-windows-373339cb-bf1a-4509-b296-802a39d801dc

![image](https://github.com/user-attachments/assets/eecf4b0e-1f4b-40d1-b17f-b6ab81f8d280)

![image](https://github.com/user-attachments/assets/3bf9edb0-acf8-4759-8627-655f3f81697b)

When pushing send: 
![image](https://github.com/user-attachments/assets/7e964718-7d2e-4071-b614-3c8d2782ebf4)

When choosing "Hae digitaalinen tunnus" it opens Microsoft support pages. 
When I choose "Ok", then it gives me erros message.

![image](https://github.com/user-attachments/assets/60a4daae-d544-48e1-aa18-29572c65fb46)

Basically what should happen is that I encrypt my message and give the email receiving person my public key. With that key the email receiver can open my message. The security of encrypting mail in Outlook seems decent. It uses 




![image](https://github.com/user-attachments/assets/a8be0595-a0c0-4c60-a36f-0e77cca00f8f)




d) Eve and Mallory.
Encryption prevents anyone from reading your message. Signing protects your message from modification. Public keys allow you to establish trust without meeting physically.
Protection against Eve: Generating keypairs for both Alice and me. Alice want's to send me a message. For this, she needs my public key. I'll export it. Parameters to export are
--export Export my public key
--armor Only use ASCII characters, so that the output can be viewed and copy -asted.
--output tero.pub Save the output into the file "tero.pub"
Alice can check the fingerprint to verify that this is indeed Tero's key. This step is needed if Tero's public key was obtained over insecure channel, like unencrypted email, a web page or a key server. Alice signs Tero's key to mark it as trusted. Now that Alice has Tero's key, she can encrypt messages to Tero.

Protection against Mallory: Alice needs Tero's public key to encrypt. Tero needs Alice's public key to verify Alice's singature. And vice versa. Alice wants to sign her messages. Tero needs Alice's key to know that it's really her. The process for exporting, importing, verifying and trusting the key is the same as before. Only the roles have been swapped. The initial steps of establishing trust are completed. Tero and Alice have exchanged keys, and verified that they have the correct keys. 
The parts of the command are: 
--encrypt Encrypt the message
--recipient tero@example.com.invalid To key identified by email address.
-sign Sign the message using Alice's secret key. 
--armor Use normal, printable ASCII characters for the message. This way, we can copy-paste it, and it does not break if we send it in email body. It uses base64 to show binary data using normal letters.
--output encrypted.pgp Save the encrypted message to this file
message.txt The plain text file we wish to encrypt
The encrypted message starts with "BEGIN PGP MESSAGE" and ends with "END PGP MESSAGE". The 20+ lines of gibberish in between is Alice's secret message, encrypted, signed and ASCII armored.
The message was decrypted with Tero's secret key. Now Tero can read the message: "Hi Tero, This is my secret...". Alice's signature was verified using Alice's public key. Now Tero knows it's really her.

f) Password management. Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)

g) Refer to sources. 
Done. 

# First homework Adversarial mindset
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

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

I tried to follow instructions but in real life it was different from instructions all the time. I could download the right debian image. Right after that I got error from missing some python part. I continued installation of virtual machine. It made it 32 bit. I tried to document all the phases and print windows I got. It didn't ask same questions as in instructions. For a while it showd that I have the new virtual machine but pretty soon it turned to status aborted. It happened when I doubleclicked on it first time. When I tried it again, image flashes on the screen but can't tell what it is. Nothing happens. At this point I stopped trying. 

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

Reference: https://terokarvinen.com/2021/install-debian-on-virtualbox/

Try number 3 on 5.11.2024

![image](https://github.com/user-attachments/assets/5dad6970-90e3-499a-aab8-e419287a6a05)

![image](https://github.com/user-attachments/assets/0ae2b5b6-0fa6-4000-8eac-7430b3210414)

![image](https://github.com/user-attachments/assets/f31233d3-75de-476e-bd27-bb23468b0bfd)

![image](https://github.com/user-attachments/assets/21b0c780-9f16-499c-8333-e4b29481cb52)

No expert install was available. 
![image](https://github.com/user-attachments/assets/5f663296-1673-479c-a7d1-aa4dd4e513cc)

![image](https://github.com/user-attachments/assets/0dbc5d17-a163-4b66-b64e-32a0a0557eb9)

![image](https://github.com/user-attachments/assets/3a8ed31a-a1ce-43ae-b6b2-11675c1e921a)

![image](https://github.com/user-attachments/assets/61b0cf96-6545-4f2e-b1ad-b1573f0903a4)

At this point it didn't let me to finish installing

Tried again and find expert mode and now

![image](https://github.com/user-attachments/assets/d472a1b5-47ab-4375-9b4c-824da0637985)

![image](https://github.com/user-attachments/assets/b6e9bf11-d83f-4f85-8bc9-58a82cefdbcd)

![image](https://github.com/user-attachments/assets/1051eebf-6797-4696-b18a-1c9b70c34465)

![image](https://github.com/user-attachments/assets/e4ecd8e0-3047-4e51-bc63-96174b5da42a)

![image](https://github.com/user-attachments/assets/bed7fe32-a8fa-4756-ac39-ac97c7b65a83)

Then I tried to reset the machine
































