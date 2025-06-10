# Crack-the-hash_tryhackme_walkthrough
Cracking hashes challenges

## Level - 1 :
Can you complete the level 1 tasks by cracking the hashes?

I have used Tunnelsup Hash Analyzer for checking which hashing algorithm was used.

Q1. 48bb6e862e54f2a795ffc4e541caed4d

![image](https://github.com/user-attachments/assets/75fc7d23-b617-4514-9e13-c3d0736cd871)

I went to search for MD5 decrypter online and found the result:

![image](https://github.com/user-attachments/assets/8105ea44-d45d-4301-8d65-da9a90df311f)

Q2. CBFDAC6008F9CAB4083784CBD1874F76618D2A97

![image](https://github.com/user-attachments/assets/c7855d90-f7c8-4809-ba48-f2f9a1dd8e25)

I went to search for SHA1 decrypter online and found the result:

![image](https://github.com/user-attachments/assets/bc0975a6-98f3-4a8a-ab7e-0b55deebca46)

Q3. 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032

![image](https://github.com/user-attachments/assets/5d7da455-a07a-459c-9301-7d7525b255db)

I went to search for SHA2-256 decrypter online and found the result:

![image](https://github.com/user-attachments/assets/662529ed-e45f-43d6-94ea-577eaa93b399)

Q4. $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom

![image](https://github.com/user-attachments/assets/869678a5-115c-4990-bf45-0ea52098560d)

I went to search for hashes.com and found the result:

![Capture](https://github.com/user-attachments/assets/bb98cd45-2615-4fee-a0b3-7c2f72144298)

Q5. 279412f945939ba78ce0758d3fd83daa

![image](https://github.com/user-attachments/assets/a4aa8c00-c867-4500-a63c-738d6ce6aaf5)

I went to search for hashes.com and found the result:

![Capture_1](https://github.com/user-attachments/assets/8584ca65-707c-461e-ad37-bc2601aac265)

## Level - 2 :

This task increases the difficulty. All of the answers will be in the classic rock you password list.

You might have to start using hashcat here and not online tools. It might also be handy to look at some example hashes on hashcats page.

### Command : ** hashcat -m (hash mode) -a 0 (.txt file saved with given hash) /usr/share/wordlists/rockyou.txt **

Q1. Hash: F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85

![image](https://github.com/user-attachments/assets/95edff69-6c7c-482c-87d3-2ef150066e4f)

As it is SHA256 the mode for it is 1400

![image](https://github.com/user-attachments/assets/ae7598be-48ca-4efc-8887-298f1ffa5f72)

![image](https://github.com/user-attachments/assets/808ed966-b433-438e-8d06-69ceac0ef522)

Q2. Hash: 1DFECA0C002AE40B8619ECF94819CC1B

![image](https://github.com/user-attachments/assets/1d0d966d-50b8-432b-8bd6-e38dc72afa5b)

As it is MD5/MD4 the mode for it is 0/900

First, trying with MD5 using the mode 0

![image](https://github.com/user-attachments/assets/22a0ac1a-b57c-4f28-8063-42fc3b42f31c)

![image](https://github.com/user-attachments/assets/2b78ba5c-79a4-406d-b6f9-2831d9ee6730)

Let's try with MD4 with the mode 900

![image](https://github.com/user-attachments/assets/342975c6-1b7e-4fc6-8204-e4b5bb761f49)

![image](https://github.com/user-attachments/assets/9ad8f9e3-2908-41b1-8ea7-1acf39efd1eb)

Again failed, by googling it, I found it was NTLM hash.

For NTLM hash the mode is 1000

![image](https://github.com/user-attachments/assets/4ccfa4ca-7d80-40c9-8200-e5c3589bb6cb)

![image](https://github.com/user-attachments/assets/b5286488-96ba-4ae9-96eb-e10a8111756a)

Q3. Hash: $6$aReallyHardSalt$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02.

Salt: aReallyHardSalt

The first $6$ represents the code. 

Here $6$ is for SHA512.

For SHA512 the mode is 1760

![image](https://github.com/user-attachments/assets/f0ac37ad-f63f-4506-92e5-0bc66fe853da)

Next I found this, there are various modes in hashing

![image](https://github.com/user-attachments/assets/d7ed793f-d77e-47dd-b129-289eddd5f06e)

So I tried -m 1800 as it was close to the format that was given:

![image](https://github.com/user-attachments/assets/9130f514-3eef-4a42-86a1-eda9c32d9b8b)

Q4. Hash: e5d8870e5bdd26602cab8dbe07a942c8669e56d6

Salt: tryhackme

![image](https://github.com/user-attachments/assets/b1909f0d-51e7-4214-9e21-7aecdda78204)

Since salt is given so I checked for different modes:

![image](https://github.com/user-attachments/assets/bfa3d054-6b91-48c7-9f52-eefc057217b5)

![image](https://github.com/user-attachments/assets/34be6f83-c823-458e-bc4b-49ec72442ef2)






------------------------ It was a joyful learning with a bit of help from the hints. Hope you enjoyed, I did.  ------------------------------
