# Offensive Security Certified Professional (OSCP) Certification PWK Course and Exam Review

So recently, I decided to enroll for 90-days in Offensive Security's OSCP Certification program, as described by Offensive Security:

The Offensive Security Certified Professional (OSCP) is the companion certification for the Penetration Testing with Kali Linux training course and is the world’s first completely hands-on offensive information security certification. The OSCP challenges the students to prove they have a clear and practical understanding of the penetration testing process and life-cycle through an arduous twenty-four (24) hour certification exam.

They were absolutely right, it definitely was a challenge.  I can't say I've taken a course or program that has pushed me as hard as this course did over the 90 days but in the end I can see the value in learning this way and learned an incredible amount in such a short amount of time.

## About Me
Follow me on Twitter! **@416Security || https://twitter.com/416security**

I've been in the Information Security realm for around 5 years, the first few years focusing on doing consulting, architecture and deployment, the latter few focusing heavily on management, auditing and compliance.  As I got more into the management side of things, I felt my techincal edge which had gotten me so far along in my career starting to slip, which is how I found myself signing up for the OSCP certification program.

## Course Outline

The course is outlined in the Syllabus in the Resources section below, but logically I broke it up into 3 main sections:

1. Course Material (Video/PDF) - documentation provided by Offensive Security upon starting the program.
2. The Lab Environment - access to the lab environment is provided by Offensive Security upon starting the program.
3. The Final Exam - provided at the start of your exam.

I'll go through some of the strategies I took and how they worked out further on.

### Resources

* PWK Syllabus: https://www.offensive-security.com/documentation/penetration-testing-with-kali.pdf

## Before Starting the Course

I wasn't really sure what to expect from the course in terms of difficulty level and experience required.  After much research I found the best way to practice (especially if you have an ESXi server at home!) was to attack vulnerable machines created by others and get familiar with some of the tools of the trade and practice some basic programming.

Two resources stood out for this (links are in the Resources section):
1. Vulnhub - a repsoitory of vulnerable machines.
2. HackTheBox - a pentesting lab of hosted vulnerable machines.

For Vulnhub virtual machines, I had found a blog created by **abatchy** which listed a number of similar machines to what would be found in the OSCP.  About a month prior to starting the course I started going through these.  A huge thing about these machines is that they have publically available walkthroughs.  To be honest, I couldn't hack many of them and had to follow walkthroughs for a bunch of the systems, but took good notes and learned alot from just going through the walkthroughs.

For HackTheBox, first you need to solve a puzzle to get yourself an invite code.  Once you're able to do this you're presented with VPN access to their lab.  The issue I had with this site as great as it is, is that you'll have a bunch of users attacking the same machine which can often be reverted in the middle of working on something.  In hindsight I could've paid for a subscription which would have likely solved this problem but with my start date around the corner I decided against it.  I was still able to root around 10-12 machines with relative ease as preparing with the Vulnhub VMs was an excellent training method.

### Resources
* abatchy's OSCP-like Vulnhub VMs - https://www.abatchy.com/2017/02/oscp-like-vulnhub-vms.html
* HackTheBox - https://www.hackthebox.eu/

## Getting Through the Material

The day finally arrived where I recived teh e-mail I had been waiting what seemed like a long-time for:

* Welcome to the Penetration Testing with Kali Linux (PWK) online course! *

After poking around the lab environment a bit I realized that jumping right in may not be the best idea, I feel I was correct.  I spent the next 14 days going through the videos and PDF and completing what exercises I could and flagging which excercises I couldn't as I'd need to explore the labs more in order to complete a few execercises.  

I feel a lot of people may just skim this material and want to jump right into the labs, I don't blame you but this is a **huge** mistake.  Many of the methods outlined in the documentation are exactly what you need in the labs and exam.  There is a huge amount of self-learning involved in this course, however, skimming the documentation is seriously ill advised.

### Resources

* PWK Syllabus: https://www.offensive-security.com/documentation/penetration-testing-with-kali.pdf

## Getting Through the Lab Environment

So you've gotten through the basic excercises, great!  Now to put those skills to the test.  I can tell you that in my 90-days I managed to get admin/root on every single box in all the lab networks.  I cannot stress this enough, you **do not want to underestimate** how much time is required to really go far in the labs.  A few notes you'll want to keep in mind when it comes to the labs:

* Start with the low-hanging fruit.
* Do proper and thorough enumeration of system services, if your enumeration is wrong or incomplete you will likely was **a lot** of time doing things that won't work.
* Do a proper post-enumeration on compromised machines, password re-use does exist and sometimes is the dependancy you'll need to access another machine.
* Document everything, exploit attempts, failed attempts, passwords recovered, who the machine talks to etc.
* Dual-homed machines **simplify** things greatly when it comes to accessing other networks.
* Take the time to understand the firewalls and the roles they play in each of the networks - this can save you some degree of headaches when things just aren't working properly.
* When it comes to privilege escalation, learn to identify what is wrong or out of place - this really is gained through experience.
* If you're stuck, research, be patient and TRY HARDER.

Working on machines in the labs would take me right up to my exam date which was 4 days after my lab access expired.  Some of my most memorable days were:

* Fully compromising the entire Development department network in one day.
* Fully compromising the big 4 (PAIN, SUFFERANCE, GH0ST, HUMBLE).
* JACK.

Out of all the machines in the lab, JACK was my nemesis.  I literally gave up on it, it was the last machine in the lab left for me to compromise and after about a week of on and off trying I gave up and focused my time on getting the documentation done for the PWK exercises and lab report as I hadn't even gained a foothold into this box.  Once the documentation was done, I had 2 more days of lab time and decided to take one last stab at JACK after going so far into the labs I had gotten a bit cocky and slacked a bit on my enumeration - this slacking cost me a lot of time and effort!  I started over from scratch and found the thing I needed to gain a foothold, once that happened within an hour I was root on JACK.  I had done it, rooted every lab box.

There are times when frustration and exhaustion will kick in, taking breaks helped me a lot, so many times the solution would come to me while out walking my dog instead of mindlessly pounding away at the keyboard.

Personally, I'd recommend everyone go as far as they can into the labs and try to get every machine - some might say it won't help on the exam, I'd disagree.  The more exposure you have to different systems and vulnerabilites and privilege escalation methods are higher the odds that you'll be able to quickly identify a vulnerability and exploit it when it comes to the exam.  For me, the real OSCP Lab began after owning 39 boxes and being forced to pivot to access more.

## A Note About Documentation

* Do not underestimate how long documentation takes!  
* Do not leave it for the last minute!  

Even if you have all the notes you want to have it formatted nicely and ensure it's correct.  For the lab machine write-up I ended up going back and re-hacking a few machines in order to get the proper screenshots and information.  In total, I'd say it took about 3 full days to complete my 10 machine lab write-up and the remaining exercises.  Trust me, the lab report was around 150 pages and I cut alot out for the sake of brevity.

When it came to the exam, I had learned my lesson and documented as I went but even this took a few hours longer than I'd like.

For note taking I used the popular CherryTree, each individual system had the following template which can be found below as well: 

1. Enumeration
   - TCP
   - UDP
   - Web Services
     - nikto
     - Dirb/DirBuster
     - WebDav
     - CMS
   - Other Services
     - SMB
     - SNMP
     - DB
     - Other
2. Exploitation
3. Post Exploitation
   - Script Results
   - Host Information
   - File System
   - Running Processes
   - User & Groups
   - Network
   - Scheduled Jobs
4. Priv Escalation
5. Goodies
   - Hashes
   - Passwords
   - Proof
6. Software Versions
7. Log Book

Below is a list of links that helped me immensely during going through the labs:

## A Note About MS17-010

You might find this a lot in the labs. From my understanding it isn't part of the course - you can definitely test it out and learn about it but I'd treat it like Metaspoit usage and not become reliant on it.

### Resources

#### Documentation
* OSCP Reporting Templates - https://support.offensive-security.com/#!pwk-reporting.md
* CherryTree - https://github.com/giuspen/cherrytree
* James Hall CTF Template - https://411hall.github.io/assets/files/CTF_template.ctb
* James Hall OSCP Writeup - https://411hall.github.io/OSCP-Preparation/

#### Enumeration
* OneTwoPunch - https://github.com/superkojiman/onetwopunch
* SNMP Commands - https://docs.oracle.com/cd/E19201-01/820-6413-13/SNMP_commands_reference_appendix.html
* Nmap cheatsheet - https://highon.coffee/blog/nmap-cheat-sheet/

#### Privilege Escalation
* g0tm1lk Basic Linux Privilege Escalation - https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/
* FuzzySecurity Windows Privilege Escalation Essentials - http://www.fuzzysecurity.com/tutorials/16.html
* xapax Windows Privilege Escalation - https://xapax.gitbooks.io/security/content/privilege_escalation_windows.html
* 1N3 Linux Privilege Escalation Scripts - https://github.com/1N3/PrivEsc/tree/master/linux/scripts

#### Exploitation
* Reverse shell cheatsheet - http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet
* msfvenom cheatsheet - http://security-geek.in/2016/09/07/msfvenom-cheat-sheet/
* Manually Exploiting MS17-010 - https://lmgsecurity.com/manually-exploiting-ms17-010/
* Restricted shell escaping - https://fireshellsecurity.team/restricted-linux-shell-escaping-techniques/
* Accessing MSSQL from KALI - https://www.adampalmer.me/iodigitalsec/2013/08/10/accessing-and-hacking-mssql-from-backtrack-linux/
* Identify Ubuntu Version by SSH Banner - http://auntitled.blogspot.com/2010/07/identified-ubuntu-version-from-ssh.html

## Getting Through the Final Exam

So the another big day finally came.  In my 4 day downtime I had spun up a Windows 7 machine to practice some Buffer Overflow exercises on and warmed up on a few Vulnerable VM's from Vulnhub which I tore through in succession.  It was quite the feeling when I came to realization that 90-days ago I had to refer to walkthroughs for these machines and now was able to root them with relative ease.

I went grocery shopping the night before, made sure I had a good nights rest, and everything I'd need nearby. I got up at 9:00AM and geared up to start the Exam at 10:00AM.  Right on schedule an email from Offenseive Security arrived in my inbox and off I went.  Like many writeup's I've read, I too started on the Buffer Overflow box which kept freezing for some reason, but I was able to work through it.  While working on this, I was enumerating the other systems in the background.  I read somewhere a piece of advice for this exam, that if you're only doing one thing at a time - you're doing it wrong.  I made the most of my time but multitasking where I could.

Without going into much detail, my timeline went as follows: 

- 90 minutes - 25 points.
- 3 hours - 35 points.
- 4.5 hours - 55 points.
- 7 hours - 75 points.

After 7 hours I was able to collect enough points to cross that 70 point threshold.  I spent the next 8 hours prodding the last machine but could not find a way in.  I was really burnt out at this point, perhaps the excitement, perhaps the lack of well timed breaks - I tried to break every 2 hours for 10 minutes or so.  Either way, I didn't see a way in that night to the last machine so I started going through the rest of the machines I'd compromised and made sure all my documentation was on point.  I'd hate to fail this thing for missing a step somewhere or having poor documentation so I used up the VPN time to gather everything I'd need.

The next day I sent off my documentation and eagerly awaited for the next 48 hours.

## Aftermath

Around 30 hours later, this arrived:

*We are happy to inform you that you have successfully completed the Penetration Testing with Kali Linux certification exam and have obtained your Offensive Security Certified Professional (OSCP) certification.*


### Resources

Any questions or concerns, drop me a line on Twitter! **https://twitter.com/416security**
