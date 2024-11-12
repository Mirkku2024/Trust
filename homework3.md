# Trust
Homework reports for security course taught by Tero Karvinen

# Third homework Hash
Reference: https://terokarvinen.com/trust-to-blockchain/#homework

# Summary from Schneier 2015: Applied Cryptography: Chapter 2 - Protocol Building Blocks: subchapters 2.3 and 2.4
2.3 One-way Fuctions
One-way function is basic element to public-key cryptography. Those are easy to make but very difficult if not impossible to reverse. You can't use only one-way function to message encrypting because no one could decrypt it. 

2.4 One-Way Hash Functions
- A one-way hash function is an essential part of modern cryptography.
- A hash function is a function that uses input string (called a pre-image) whatever length and converts it to a fixed-length which is usually smaller output string. That is a hash value. It is a fingerprint of pre-image and proves it's the correct pre-image.
- When using a one-way hash function you can't generate same hashes for different pre-images. So it doesn't collide with anything.
- The hash-function is public.
- If two parties has the same file, they can confirm it's the same because they have same hashes of the file.
- A message authentication code (MAC) is a one-way hash function but it has also a secret key. The hash value is a function of both the pre-image and the key. Someone with the key can verify the hash value.

Reference: Schneier, P. Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition. 2015. Wiley. Readable: https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/ Read: 10.11.2024

# Summary from Karvinen 2022: Cracking Passwords with Hashcat
- Systems don't store original passwords, they store hashes. Hashing is a one way function, so you can't turn it back to password. With Hashcat you can try to guess password.
- When you are making penetration testing be sure to do it according to law. Take note also an ethical point of view.
- Install Hashcat and use a big dictionary in cracking passwords.
- Identify hash type
- Crack the hash
- Hashcat reports it as solved when you have made the cracking correctly like in example case of this assignment.

Reference: https://terokarvinen.com/2022/cracking-passwords-with-hashcat/

## Other subtasks from lesson 3

a) Billion dollar busywork. Command 'echo -n "hello"|sha256sum' prints a hash. Try adding something to the string, e.g. 'echo -n 'hello asdf'|sha256sum'. What do you have to add to get a hash that starts with a zero? 
![image](https://github.com/user-attachments/assets/b14ba1f1-e626-4a3f-9603-8b875e520a93)
![image](https://github.com/user-attachments/assets/6e7d7373-3f97-4c48-ac83-facb4a2af41b)
After 23 tries still no luck with a zero in the start. Tried to google help but no luck.

b) Compare hash. Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). Change one letter. Take the hash again. Compare hashes. What do you notice?

![image](https://github.com/user-attachments/assets/7975da4b-25ac-434e-8138-23b779b71eca)

So I changed the file so that I took one letter of it and nothing changed in hashes. I wasn't sure if I should have changed the files subtitle or something in the command promt so I did only the change inside the file.

c) Hashcat. Install hashcat and test that it works.

![image](https://github.com/user-attachments/assets/f2c4917d-5273-402e-91da-9040ede7f2b4)

![image](https://github.com/user-attachments/assets/28b7d81a-ffe1-4fd4-bf4b-941b672b3366)

I cracked it.

Reference: https://terokarvinen.com/2022/cracking-passwords-with-hashcat/

d) Dictionary attack. Crack this hash: 21232f297a57a5a743894a0e4a801fc3
Well the hashcat assignment I did on sunday but on tuesday it apparently doesn't work anymore. I don't know hat should I do, in linux I found hashcat on program files.
![image](https://github.com/user-attachments/assets/f4d232ac-f491-4803-b4b6-7f0f35dd30e6)


e) How can you make a password that's protected against a dictionary attack?
Generate a password and store it with some password manager to keyvault.

j) John. Install Jumbo John (John the Ripper, open source Jumbo version). Compile it from source code as needed. See Karvinen 2023 Crack File Password With John.
Ei tainnut onnistua asennus
![image](https://github.com/user-attachments/assets/7907c089-6c4b-4144-b279-4a11d2b8c6f6)
Olisin kokeillut jatkoa, mutta jostain syystä näppäimistöni ei anna erikoismerkkejä normaaleilla tavoilla, vaikka asennusvaiheessa valitsin näppäimistön kielen ohjeen mukaan. Tällä kertaa en saa muodostettua ohjeen mukaista komentoa, sillä en saa millään näppänyhdistelmällä yhtäsuuri merkkiä = eikä anna kopioida muista lähteistä mitään Linux komentoihin 
$ git clone --depth=1 https://github.com/openwall/john.git

Reference: https://terokarvinen.com/2023/crack-file-password-with-john/

k) Crack file password with John.
Ks. edellinen
