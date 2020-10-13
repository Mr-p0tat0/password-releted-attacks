# 10 Most Popular Password Cracking Tools 

## What is password cracking?
A well-designed password-based authentication system doesn’t store a user’s actual password. This would make it far too easy for a hacker or a malicious insider to gain access to all of the user accounts on the system.

Instead, authentication systems store a password hash, which is the result of sending the password — and a random value called a salt — through a hash function. Hash functions are designed to be one-way, meaning that it is very difficult to determine the input that produces a given output. Since hash functions are also deterministic (meaning that the same input produces the same output), comparing two password hashes (the stored one and the hash of the password provided by a user) is almost as good as comparing the real passwords.

## Techniques of password cracking:
- Dictionary attack: Most people use weak and common passwords. Taking a list of words and adding a few permutations — like substituting $ for s — enables a password cracker to learn a lot of passwords very quickly.
- Brute-force guessing attack: There are only so many potential passwords of a given length. While slow, a brute-force attack (trying all possible password combinations) guarantees that an attacker will crack the password eventually.
- Hybrid attack: A hybrid attack mixes these two techniques. It starts by checking to see if a password can be cracked using a dictionary attack, then moves on to a brute-force attack if it is unsuccessful.

# Tools used for password cracking:
## 1. Hashcat
Hashcat is one of the most popular and widely used password crackers in existence. It is available on every operating system and supports over 300 different types of hashes.Hashcat enables highly-parallelized password cracking with the ability to crack multiple different passwords on multiple different devices at the same time and the ability to support a distributed hash-cracking system via overlays. 
Installation : 
`````
apt install hashcat
``````
 Basic syntax for usage :
`````
hashcat -m [hash type] [txt file containing hash] [wordlist]
``````
Reference link: https://github.com/hashcat/hashcat


## 2. John the Ripper
John the Ripper is a well-known free open-source password cracking tool for Linux, Unix and Mac OS X. A Windows version is also available. 
John the Ripper offers password cracking for a variety of different password types. It goes beyond OS passwords to include common web apps (like WordPress), compressed archives, document files (Microsoft Office files, PDFs and so on), and more.

Installation guide : https://www.openwall.com/john/pro/linux/

Basic usage:
```````
john --wordlist=password.lst --rules passwd
````````
Reference: 
https://www.openwall.com/john

## 3. Brutus
Brutus is one of the most popular remote online password-cracking tools. It claims to be the fastest and most flexible password cracking tool. This tool is free and is only available for Windows systems. It was released back in October 2000.
Brutus supports a number of different authentication types, including:

- HTTP (basic authentication)
- HTTP (HTML Form/CGI)
- POP3
- FTP
- SMB
- Telnet
- IMAP
- NNTP
- NetBus
- Custom protocols
It is also capable of supporting multi-stage authentication protocols and can attack up to sixty different targets in parallel. It also offers the ability to pause, resume and import an attack.
 
Reference link: https://www.darknet.org.uk/2006/09/brutus-password-cracker-download-brutus-aet2zip-aet2/

## 4.RainbowCrack
All password-cracking is subject to a time-memory tradeoff. If an attacker has precomputed a table of password/hash pairs and stored them as a “rainbow table,” then the password-cracking process is simplified to a table lookup. This threat is why passwords are now salted: adding a unique, random value to every password before hashing it means that the number of rainbow tables required is much larger.
RainbowCrack is a password cracking tool designed to work using rainbow tables. It is possible to generate custom rainbow tables or take advantage of preexisting ones downloaded from the internet. RainbowCrack offers free downloads of rainbow tables for the LANMAN, NTLM, MD5 and SHA1 password systems.

You can get tool here: http://project-rainbowcrack.com/

## 5. Aircrack-ng
Aircrack-ng is a Wi-Fi password-cracking tool that can crack WEP or WPA/WPA2 PSK passwords. It analyzes wireless encrypted packets and then tries to crack passwords via the dictionary attacks and the PTW, FMS and other cracking algorithms. It is available for Linux and Windows systems. A live CD of Aircrack is also available.

Installation guide: 
``````
sudo apt-get install build-essential autoconf automake libtool pkg-config libnl-3-dev libnl-genl-3-dev libssl-dev ethtool shtool rfkill zlib1g-dev libpcap-dev libsqlite3-dev libpcre3-dev libhwloc-dev libcmocka-dev hostapd wpasupplicant tcpdump screen iw usbutils
````````
Basic usage :
`````
aircrack-ng -w [wordlist] -b [mac address] [handshake captured file]
```````
Note: This tool mainly used for cracking wifi password and it has multiple requirements, make sure you have all installed.

Reference: https://github.com/aircrack-ng/aircrack-ng

Happy hacking :)


