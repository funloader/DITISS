Offensive Security Intro
Hack your first website (legally in a safe environment) and experience an ethical hacker's job.


What is Offensive Security?
"To outsmart a hacker, you need to think like one."

This is the core of "Offensive Security." It involves breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access. The goal is to understand hacker tactics and enhance our system defences.

Beginning Your Learning Journey

In this TryHackMe room, you will be guided through hacking your first website in a legal and safe environment. The goal is to show you how an ethical hacker operates.

Our labs can also be reverted to their initial state, so don't be afraid to break the machine. Experiment as much as you like, we got you covered!

Answer the questions below
Which of the following options better represents the process where you simulate a hacker's actions to find vulnerabilities in a system?

Offensive Security
Defensive Security
Offensive Security

Correct Answer

Briefing

Our goal is to find a way to hack the FakeBank application to steal money. For that purpose, they have provided us with an account in the bank, just as if we were a regular user.

One of the easiest ways we can try to hack the application is by finding hidden features in the application. Sometimes, applications will expose sensitive functionality to users via secret URLs. If we can find such URLs, we might be able to perform actions that a regular user is not supposed to do.

The output of the command might look a bit intimidating, but here's a simple breakdown of what is reported:

The first section of the output tells us the URL_BASE we scanned, which is just the URL we gave the tool. It also shows the location of the wordlist file used by the tool, which contains common page names that will be tested during the brute-force attack. In this case, the tool uses the default wordlist included with the tool, located at /usr/share/dirb/wordlists/common.txt. There's a copy of the common.txt file in your desktop as well, if you want to explore it.

To find hidden URLs, we will use a tool called dirb. This tool uses a brute-force approach, by taking a list of potential page names and testing one by one if they exist in your website. This approach works because people use predictable names a lot of times.

Using dirb To Find Hidden Website Pages

Using dirb is quite simple. Using the terminal, write the dirb command followed by the URL of the website you want to brute-force. Be sure to press ENTER in your keyboard to execute the command:


Defensive Security Intro

Introducing defensive security, what it involves and looks like within the real-world, as well as the technologies involved.

Task 1
Introduction to Defensive Security


In this room, we will explore the world of defensive security (also known as blue teaming). We will uncover how defensive security teams play a key role in protecting networks and organisations across the globe, and understand what defensive security looks like in practice.

Unfortunately, headlines show us what happens when defensive security falls short. From large-scale ransomware attacks on healthcare systems to data leaks at major corporations, the impact of poor security can be severe and incredibly costly for an organisation, with fines to follow. Here are some real-world examples:

 
British Airways (2018)

Personal details such as birth names, addresses, and payment card details of 400,000+ customers were leaked. 

British Airways was fined £20 million for this incident.
 
Marriott International (2020)

The passport information, payment card details, and names of 334 million customers were leaked, partly due to outdated systems.

Marriott International settled a $52 million lawsuit.
 
Advanced Computer Software Group (2022)

Medical records and phone numbers for 79,904 people were leaked due to weak security policies.

Government officials fined the organisation £3.07 million.
 
23andMe (2023)

Over 7 million users' sensitive data, such as names, addresses, health records, and DNA data, was leaked due to poor security policies.

23andMe was fined £2.31 million by government officials.
 
SK Telecom (2024)

Poorly configured servers led to the personal data of approximately 27 million users being leaked.

SK Telecom were fined $97 million by government officials.

Answer the questions below
What is defensive security also known as?

Task 2
Responsibilites of Defensive Security
This task will explore defensive security in more depth. You will also meet some of the experts within a defensive security team to learn more about their day-to-day responsibilities.

Let's start by focusing on some key areas of defensive security:

Monitoring and Detecting

Continually observing network and system activity to detect suspicious behaviour and events.

These may include, for example, monitoring for logins from another country while the employee is based in the company's London office.
 
Incident Response

The team quickly comes together if suspicious activity is confirmed and alerts are raised.

This is when the Incident Response process begins. The process involves containing and removing the threat and restoring the business back to normality.
 
Threat Intelligence

Gathering and using information about attackers—their latest methods, targets, and trends—can greatly strengthen an organisation’s defences.

For example, understanding that an attacker focuses on a specific software application used within organisations.
 
Vulnerability Management

Fixing software or system flaws is an important preventative measure that can lower the risk of an attack.

Security teams can check which systems attackers are most likely to target. This can be done manually or with the help of automated tools.
 
Investigation and Analysis

Members of a defensive security team are always monitoring and analysing what’s happening inside an organisation.

They work to separate normal activity from suspicious behaviour, digging into the details like solving a puzzle to uncover valuable insights.

What's more, a defensive security team is made up of a mixture of roles and responsibilities. Below, let's meet some of the highly-skilled individuals you would find within a defensive security team:

 Icon
Bob, SOC Analyst

Bob monitors events on the organisation's network and systems to identify suspicious or expected behaviour.

He is at the frontline of protecting the organisation.

 Icon
Aaliyah, Incident Responder

Aaliyah is responsible for investigating and responding to ongoing security incidents within the organisation.

She will monitor and prevent attackers in real time and share lessons learned during the attack to prevent future incidents.

Icon
Zoe, Security Engineer

Zoe develops and maintains the essential tools and systems that support the defensive security team.

These systems enable the team to monitor, investigate, and explore events within an organisation.

Icon
Bill, Digital Forensics

Bill will utilise their expertise to understand what occurred during an incident.

They will gather, preserve, and analyse evidence from the network and systems to uncover vital information about the attackers and their methods.

Answer the questions below
An attack has been detected on an organisation's network. What is the name of the person above who would be responsible for responding to the attack?

Task 3
Defensive Security in Practice

Now that you’ve been introduced to defensive security and met some key individuals, let's understand how it is applied.

Organisations don’t rely on a single tool or method to stay secure — they build layers of defence, much like an onion or many layers to a castle. We call this "Defence in Depth," meaning that if one security measure fails, we have others to rely upon at various stages.

 Examples of these defensive measures include:
 
Employee Training

In today's world, the human factor of cyber security cannot be ignored.

With attacks more often than not targeting employees rather than systems, training employees to be proactive in recognising attempts for things like phishing is essential.
 
Intrusion Detection Systems (IDS)

These devices act as surveillance cameras across the organisation's IT.

They monitor and alert when suspicious behaviour or activity is detected across the network or systems.
 
Firewalls

These devices act as security guards on an organisation's network.

They monitor and determine what traffic is allowed to enter the network, or should be rejected.
 
Security Policies

Security policies help organisations ensure that their systems are used correctly.

They can reduce risk by blocking access to dangerous websites or requiring strong passwords, making it harder for attackers to guess login details.

This means that even if an employee clicks on a dangerous attachment in an email, other protections are in place to prevent the malicious attachment from harming the organisation.

Defensive security teams rely on a wide range of tools and technologies. These tools allow professionals to analyse information and investigate threats more effectively. This section will look at some key technologies commonly used by defensive security teams worldwide.

Exploring the Security Operations Centre (SOC)
Think of a SOC as the defensive security centre for an organisation's technology. This busy centre is the frontline of protecting an organisation, often operating around the clock, 365 days a year, and employs a variety of security professionals who monitor and protect the organisation's networks, systems, and data.

A typical day in the SOC could look like:

Reviewing alerts triggered by security tooling
Investigating anomalies
Responding to incidents
These professionals are often the eyes and ears on the frontline for protecting an organisation.

SIEMs: The Defensive Security Radar
Much like a control centre in the real world, SIEMs (Security Information and Event Management) systems are the central place for all data and information collected from security devices, workstations, servers, and more within an organisation.

Much like radar sweeping the digital environment, these systems are an absolutely critical part of any organisation's defensive security, as they offer insight into what is happening within the organisation's IT.

The systems inside an organisation produce a large amount of information. This information needs to be brought together in one central and easy-to-access place to understand what's happening quickly and clearly. This way, several people can review and analyse it quickly.

Answer the questions below
What is the abbreviation for the term "Security Operations Centre"?

Careers in Cyber
Learn about the different careers in cyber security.

Task 1
Introduction
Want a career in cyber security? Explore what that could look like for you
Cybersecurity has many career paths, from breaking into systems (offensive security) to defending organisations from attacks (defensive security).



You don’t need a specific background to start. If you enjoy solving problems, being curious, or understanding how things work, you’ll likely find a role that fits you.

Why get a career in cyber:

High demand: over 3.5 million unfilled roles.
Strong salaries: competitive pay even at entry level.
Constant learning: the field evolves fast.
Are you ready to learn more about some of the leading roles involved in cyber security? Let's begin!

Answer the questions below
How many unfilled cyber positions are there?

Task 2
Security Analysis
Read further if you are
Detail-Focused, Curious and Love Puzzles

Security analysts are often referred to as the digital defenders of an organisation and sit on the blue team. These people monitor, investigate and respond to activity taking place on an organisation's devices and network, and play a significant role in an organisation's defence.

Using their skills, security analysts investigate and piece together potential security incidents, known as alerts, to decide if further action is needed and respond appropriately.

An example of a potential security incident is an employee who works in the London office who suddenly logs in from another country. An investigation is required to determine if this is legitimate.

Not only that, but security analysts are one of the most in-demand roles within cyber security, offering a long and rewarding career path.

A Typical Day as a Security Analyst Involves:
Monitoring activity taking place on the devices and network of the organisation.
Investigating unusual or suspicious activity, such as strange logins.
Piecing together information to understand what has happened, when, and how.
Working with other teams to improve the organisation's defences.
Progression
Security Analyst is a broad entry point into defensive security, with many paths to specialise later. You can move into areas like threat hunting, incident response, or malware analysis. Incident responders handle active attacks, while malware analysts examine the tools and code used by attackers.

Answer the questions below
Security analysts play a significant role in an organisation’s _____?
defence

Task 3
Security Engineering
This role could be for you!
If You Enjoy Problem-Solving and Building Things
At a high level, Security Engineers build and maintain the systems and processes that protect an organisation's network and devices and are known as the architects of cyber security. 

For example, a Security Engineer will be responsible for maintaining an Intrusion Detection System (IDS), which can be considered a security camera within an organisation's digital environment.

Systems like these use a mixture of rules and intelligence to detect and prevent attacks from occurring.

A Typical Day as a Security Engineer Involves:
Designing and maintaining security systems.
Keeping up to date with the latest and greatest hacker techniques being used.
Documenting processes and procedures.
Assessing risk and making sure systems and applications are protected against vulnerabilities.
Progression
Security engineering is already a specialised defensive role, but you can go even deeper into areas like application security or cloud security. The skills you build here also transfer well into other fields, including offensive security.

Answer the questions below
What is the name for the type of device that a Security Engineer would be responsible for maintaining?

Task 4
Penetration Testing
This may align with you!
Are You Methodical and Curious?

You may hear penetration testing referred to as “pentesting” or “ethical hacking.” A penetration tester’s job is to check how secure a company’s systems and software are by safely trying to break into them.

They search for weaknesses and vulnerabilities and then test if those can be exploited - just like a real hacker would, but in a safe and controlled way. Everything is done under an agreement between the company and the pentester. This process is known as an engagement. 

The results of these tests help the company understand risks and address problems before real cybercriminals can exploit them.

A Typical Day as a Penetration Tester Involves:
Testing the security of computer systems, networks, and websites.
Performing security assessments, audits, and analysing security policies.
Analysing the results and creating reports, advising an organisation on how to prevent the attack from occurring.
Progression
Penetration testing is a strong starting point for an offensive security career. You can specialise in areas like network or web application testing, and later progress into red teaming, where you simulate full-scale, long-term attacks across an entire organisation, sometimes even involving physical intrusion. Red teaming is a senior, advanced progression from pentesting.

Answer the questions below
What process do penetration testers follow when testing an organisation for weaknesses?

What is Networking?
Begin learning the fundamentals of computer networking in this bite-sized and interactive module.

Task 1
What is Networking?
Networks are simply things connected. For example, your friendship circle: you are all connected because of similar interests, hobbies, skills and sorts.

Networks can be found in all walks of life:

A city's public transportation system
Infrastructure such as the national power grid for electricity
Meeting and greeting your neighbours
Postal systems for sending letters and parcels
But more specifically, in computing, networking is the same idea, just dispersed to technological devices. Take your phone as an example; the reason that you have it is to access things. We'll cover how these devices communicate with each other and the rules that follow.

In computing, a network can be formed by anywhere from 2 devices to billions. These devices include everything from your laptop and phone to security cameras, traffic lights and even farming!

Networks are integrated into our everyday life. Be it gathering data for the weather, delivering electricity to homes or even determining who has the right of way at a road. Because networks are so embedded in the modern-day, networking is an essential concept to grasp in cybersecurity.

Take the diagram below as an example, Alice, Bob and Jim have formed their network! We'll come onto this a bit later on.


Networks come in all shapes and sizes, which is something that we will also come on to discuss throughout this module. 

Answer the questions below
What is the key term for devices that are connected together?

Task 2
What is the Internet?
Now that we've learnt what a network is and how one is defined in computing (just devices connected), let's explore the Internet.

The Internet is one giant network that consists of many, many small networks within itself. Using our example from the previous task, let's now imagine that Alice made some new friends named Zayn and Toby that she wants to introduce to Bob and Jim. The problem is that Alice is the only person who speaks the same language as Zayn and Toby. So Alice will have to be the messenger!



Because Alice can speak both languages, they can communicate to one another through Alice — forming a new network.

The first iteration of the Internet was within the ARPANET project in the late 1960s. This project was funded by the United States Defence Department and was the first documented network in action. However, it wasn't until 1989 when the Internet as we know it was invented by Tim Berners-Lee by the creation of the World Wide Web (WWW). It wasn't until this point that the Internet started to be used as a repository for storing and sharing information, just like it is today.

Let's relate Alice's network of friends to computing devices. The Internet looks like a much larger version of this sort of diagram:





As previously stated, the Internet is made up of many small networks all joined together.  These small networks are called private networks, where networks connecting these small networks are called public networks -- or the Internet! So, to recap, a network can be one of two types:

A private network
A public network
Devices will use a set of labels to identify themselves on a network, which we will come onto in the task below.

Answer the questions below
Who invented the World Wide Web?

Task 3
Identifying Devices on a Network

View Site
To communicate and maintain order, devices must be both identifying and identifiable on a network. What use is it if you don't know whom you're talking to at the end of the day?

Devices on a network are very similar to humans in the fact that we have two ways of being identified:

Our Name
Our Fingerprints
Now we can change our name through deed poll, but we can't, however, change our fingerprints. Every human has an individual set of fingerprints which means that even if they change their name, there is still an identity behind it. Devices have the same thing: two means of identification, with one being permeable. These are:

An IP Address
A Media Access Control (MAC) Address -- think of this as being similar to a serial number.

IP Addresses
Briefly, an IP address (or Internet Protocol) address can be used as a way of identifying a host on a network for a period of time, where that IP address can then be associated with another device without the IP address changing. First, let's split up precisely what an IP address is in the diagram below:



An IP address is a set of numbers that are divided into four octets. The value of each octet will summarise to be the IP address of the device on the network. This number is calculated through a technique known as IP addressing & subnetting, but that is for another day. What's important to understand here is that IP addresses can change from device to device but cannot be active simultaneously more than once within the same network.

IP Addresses follow a set of standards known as protocols. These protocols are the backbone of networking and force many devices to communicate in the same language, which is something that we'll come onto another time. However, we should recall that devices can be on both a private and public network. Depending on where they are will determine what type of IP address they have: a public or private IP address.

A public address is used to identify the device on the Internet, whereas a private address is used to identify a device amongst other devices. Take the table & screenshot below as an example. Here we have two devices on a private network:


Device Name	IP Address	IP Address Type
DESKTOP-KJE57FD	192.168.1.77	Private
DESKTOP-KJE57FD	86.157.52.21	Public
CMNatic-PC	192.168.1.74	Private
CMNatic-PC	86.157.52.21
Public

https://assets.tryhackme.com/additional/cmn-aoc2020/day-8/1.png
These two devices will be able to use their private IP addresses to communicate with each other. However, any data sent to the Internet from either of these devices will be identified by the same public IP address. Public IP addresses are given by your Internet Service Provider (or ISP) at a monthly fee (your bill!)

https://assets.tryhackme.com/additional/cmn-aoc2020/day-8/2.png

As more and more devices become connected, it is becoming increasingly harder to get a public address that isn't already in use. For example, Cisco, an industry giant in the world of networking, estimated that there would be approximately 50 billion devices connected on the Internet by the end of 2021. (Cisco., 2021). Enter IP address versions. So far, we have only discussed one version of the Internet Protocol addressing scheme known as IPv4, which uses a numbering system of 2^32 IP addresses (4.29 billion) -- so you can see why there is such a shortage!

IPv6 is a new iteration of the Internet Protocol addressing scheme to help tackle this issue. Although it is seemingly more daunting, it boasts a few benefits:

Supports up to 2^128 of IP addresses (340 trillion-plus), resolving the issues faced with IPv4
More efficient due to new methodologies
The screenshot below compares both an IPv6 and IPv4 address.



MAC Addresses

Devices on a network will all have a physical network interface, which is a microchip board found on the device's motherboard. This network interface is assigned a unique address at the factory it was built at, called a MAC (Media Access Control ) address. The MAC address is a twelve-character hexadecimal number (a base sixteen numbering system used in computing to represent numbers) split into two's and separated by a colon. These colons are considered separators. For example, a4:c3:f0:85:ac:2d. The first six characters represent the company that made the network interface, and the last six is a unique number.




However, an interesting thing with MAC addresses is that they can be faked or "spoofed" in a process known as spoofing. This spoofing occurs when a networked device pretends to identify as another using its MAC address. When this occurs, it can often break poorly implemented security designs that assume that devices talking on a network are trustworthy. Take the following scenario: A firewall is configured to allow any communication going to and from the MAC address of the administrator. If a device were to pretend or "spoof" this MAC address, the firewall would now think that it is receiving communication from the administrator when it isn't.

Places such as cafes, coffee shops, and hotels alike often use MAC address control when using their "Guest "or "Public" Wi-Fi. This configuration could offer better services, i.e. a faster connection for a price if you are willing to pay the fee per device.  The interactive lab attached to this task has been made to replicate this scenario!

Practical

The interactive labs simulate a hotel Wi-Fi network where you have to pay for the service. You'll note that the router is not allowing Bob's packets ( blue) to the TryHackMe website and is placing them in the bin, but Alice's packets (green) are going through fine because she has paid for Wi-Fi. Try changing Bob's MAC address to the same as Alice's to see what happens.

Deploy the interactive lab and proceed to answer the following questions below

Deploy the interactive lab and proceed to answer the following questions below.

Answer the questions below
What does the term "IP" stand for?
Internet Protocol

Correct Answer
What is each section of an IP address called?

Octet

Correct Answer
How many sections (in digits) does an IPv4 address have? 

4

Correct Answer

What does the term "MAC" stand for?

Media Access Control

Correct Answer

Task 4
Ping (ICMP)

View Site
Ping is one of the most fundamental network tools available to us. Ping uses ICMP (Internet Control Message Protocol) packets to determine the performance of a connection between devices, for example, if the connection exists or is reliable.

The time taken for ICMP packets travelling between devices is measured by ping, such as in the screenshot below. This measuring is done using ICMP's echo packet and then ICMP's echo reply from the target device.

Pings can be performed against devices on a network, such as your home network or resources like websites. This tool can be easily used and comes installed on Operating Systems (OSs) such as Linux and Windows. The syntax to do a simple ping is ping IP address or website URL. Let's see this in action in the screenshot below.

Here we are pinging a device that has the private address of 192.168.1.254. Ping informs us that we have sent six ICMP packets, all of which were received with an average time of 4.16 milliseconds.

Now you are going to do the same thing to ping the address of "8.8.8.8" on the deployable website in this task. Pinging the correct address will reveal a flag to answer the following question below.
