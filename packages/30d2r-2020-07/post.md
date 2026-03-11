---
layout: post
title: "30D2R - July: OSINT"
date: 2021-01-04
categories: ['30D2R']
---
This post is a part of my [30 Days 2 Root](https://dev.to/sshad0w/30-days-to-root-challenge-introduction-3idp) challenge series.
Essentially, I am trying to learn the basics of a different facet of cybersecurity each month. [Click here](https://dev.to/sshad0w/30-days-to-root-challenge-introduction-3idp) to learn about how the challenge works, or tell me what I should study next!

Do you ever wonder how Twitter sleuths and private investigators can find out so much information about an event or person? Or how attackers find information that leads to a huge breach?

It's a skill that requires no programing, hacking, and it's completely legal. 

Open source intelligence (OSINT) is a very important tool of any InfoSec practitioner. It is a safe and legal way to collect information about a target because the information is accessible by anyone.


### Why do we need OSINT?

When an attacker tries to find a hole in the perimeter of a secure organization, they must gather OSINT to find the weak link. This means that the attacker needs to understand the purpose of the organization, how it's structured, and technical details about it's infrastructure.

### Passive VS active OSINT

There are two ways that information can be gathered. Passive reconnaissance and active reconnaissance. Passive recon is only using resources that do not require interaction with the target organization. This is the least risky method because there is no way the organization can trace your information gathering back to you. An example would be looking the organization up on Wikipedia to understand the basics of what the organization does, or who works for it.

Active recon gathers much more information than passive recon, but can be slightly more risky because information gathering attempts can be traced back to the attacker. Active recon can be anything from visiting the organization's website, to calling the organization, to scanning their public-facing servers to understand which services they're running.

Both are necessary to learn about the organization, but active recon requires strong [OPSEC](https://www.upguard.com/blog/opsec).

### OSINT on individuals

#### Social media
![Alt Text](/assets/img/30d2r-2020-07/img_cc7b980d40ab.png)

One of the biggest problems with the modern day internet culture is oversharing. finding basic information about someone's life like their birthday, the names of their loved ones, their interests, and other things that may help you get an initial foothold. Since a lot of people are aware enough not to overshare, a good idea is to find information about the target by finding the social media of people close to the target.


#### Username enumeration
Many people use similar usernames for every website they use. Once a username is found, it can be searched to find more websites that the target uses, and more information about the target.

#### Resumes and CVs
![Alt Text](/assets/img/30d2r-2020-07/img_fbe8a5186871.png)

Some people upload their resumes and CVs to publicly accessible places in order to increase exposure, but forget to take it down. This exposes information like their personal phone number, past residences, and possibly physical address.

#### Company records
Often times, employers will post blogs/messages about their employees (celebratory anniversary messages, project announcements, etc..) that may lead to more information about their personal and professional life.

#### Publicly available records
![Alt Text](/assets/img/30d2r-2020-07/img_00e35382366b.jpg)

Things like driving, marriage, and arrest records, birth and death certificates, and other government-related information are often publicly available. This information will vary depending which part in the world the target resides in and how the government treats that type of information.

### OSINT on organization

#### LinkedIn
![Alt Text](/assets/img/30d2r-2020-07/img_6256781e8c0c.png)

Most modern organizations list themselves on job listing sites like monster.com or LinkedIn. Finding the name of the organization on these sites will often find more employees related to the company the target works for. 

*__Protip: Enumerate internal architecture by finding the technologies used in the resumes of employees__ (ex: If someone who works for the organization states that they understand AWS, the organization might be using AWS infrastructure.)*

#### Press releases
Public press releases may lead to information about how the organization is structured, protocols for certain types of situations, and important personnel changes that may lead to a foothold.

#### News articles
News articles often contain a lot about a organization that they aren't willing to share themselves. Typically this information will be more honest, wholistic, and a different prospective than the press releases from the organization itself.

For example, a government may claim to uphold all international laws, but the news about them may state otherwise.

### Common tools and techniques

There are a million ways to find information about a person or organization with OSINT, but here are some of the things I use:

* Your favorite search engine

* [Shodan.io](shodan.io)

* [Google Dorking](https://en.wikipedia.org/wiki/Google_hacking)

* [Bloodhound](https://latesthackingnews.com/2018/09/25/bloodhound-a-tool-for-exploring-active-directory-domain-security/)

* [HaveIBeenPwned](Haveibeenpwned.com)

* News media websites

* [The Wayback machine](archive.org)

* Social media websites

* [The Harvester](https://tools.kali.org/information-gathering/theharvester)

* [Maltego](https://www.maltego.com)

* [Recon-ng/snoopy-ng](https://github.com/sensepost/snoopy-ng)

* [ExifTool](https://en.wikipedia.org/wiki/ExifTool)

* [Global Terrorism Database](https://www.start.umd.edu/data-tools/global-terrorism-database-gtd)

* [Datasploit](https://datasploit.readthedocs.io/en/latest/)

* [BRBPublications](https://www.brbpublications.com/freeresources/Pubrecsites.aspx)

* [Other sources and methods](https://www.sans.org/blog/-must-have-free-resources-for-open-source-intelligence-osint-/)

There are many ways to preform OSINT, but the best way is to use your favorite search engine. It is a very powerful tool in any hacker's toolbox that can lead to the initial foothold inside of an organization. 

Stay curious, and remember: 

*If [page two of google is the best place to hide a body](https://digitalsynopsis.com/tools/google-serp-design/), a good OSINT researcher can find the skeletons in anyone's closet.*








