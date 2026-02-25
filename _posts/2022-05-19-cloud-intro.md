---
title: "The Cloud: A Beginner's Look"
date: 2022-05-19
---
# Background

About 20 years ago, the world became a lot more "plugged in". The turn of the century brought the "dot com" era, and many businesses found that outreach was a lot easier to achieve when their advertisements, products, and services could be on the screens of the people at home all across the world.

As a response, companies invested in servers hired web developers, and put their businesses on the internet in the form of websites.

Now, "Websites are hosted on servers" is not a magical realization, and it is not new. However, there is a little more to the story.

# Server management

Server management is tedious. The most common reasons are:

* Servers take up a tremendous amount of space.
* Servers consume an incredibly expensive amount of power.
* It's difficult to troubleshoot when things go wrong. 
* Servers must be manually networked together.
For these reasons, most businesses looked for a way to cut the costs of server management.

# Introducing "The Cloud"

Enter: "The cloud". Large data-driven companies realized that they could create ways to rent out their servers in a way that multiple customers could share one resource without security breaches, or performance issues. These large companies turned around and sold cloud services to anyone who wanted to rid themselves of hardware management issues. Services like Microsoft Azure, Amazon Web Services, and Google Cloud have been the leaders for the last few decades in cloud services.

# How does the Cloud work?

In short, the cloud is nothing but a large collection of servers in an offsite data center. These are simply 3rd party resources that use the same technology and methodology as backing up your mobile phone. You (The client) have the information you'd like to back up in case something goes wrong or data you'd like to store externally. This data is offloaded to a server and kept there for later use. The client can choose when to download those resources for later use. Now there's an extension of storage space for information.

![e265e094cf8921edf3a6854d54ca7b3e.png](/assets/img/cloud-intro/0efcc887109d4a0f82285b6bced00a30.png)

## Containers
In the enterprise world, **containers are the backbone of the cloud.** These are small, easy to manage instances that perform a limited amount of tasks and take up a relatively small amount of computer power and memory. Compared to traditional hardware and virtual machines, containers are the most lightweight solution in modern computing at scale. Every container shares the resources of the underlying [kernel](https://www.techopedia.com/definition/3277/kernel), but each of them executes in isolation. In a future blog, we will go in-depth about what containers truly are, and take a more detailed look at how they work.

## Why is the cloud so popular in the enterprise?

As we've already covered, migrating to the cloud is extremely powerful and profitable for large data-driven companies, but there is no "one size fits all" solution when it comes to computational solutions. There are many different services that cloud providers will offer. Some of the most popular models are:

### Software-as-a-Service (SaaS):

SaaS is the most common service purchased in the cloud computing industry. A quick way to define it is renting software to an enterprise to use and deploy within their own environment for organizational use. Popular examples would be Office 365, Zoom (enterprise), or GitHub. All three of these companies have a model that allows their software to be used for a subscription. All of the data is stored on their servers, so the customers don't even have to worry about physical storage, only paying the annual subscription. **Imagine the SaaS client as a business that needs music for events. They rent an external band to play some select songs and use them for a fixed amount of time.**

### Platform-as-a-Service (PaaS):

If SaaS allows organizations to rent finished enterprise-level software, PaaS allows organizations to rent the tools needed to build their own software. This might look like access to specific operating systems and architecture to build new software. Common examples are Microsoft Azure, Amazon Web Services, (AWS), and Google Cloud. **Think of PaaS as the client is a music company that has some of the art tools, but they need temporary access to expensive instruments, certain musicians, and other tools. To create better music of their own.**

### Infrastructure-as-a-Service (IaaS):

IaaS is a "bare metal" solution to build software from the ground up. IaaS Clients only need a basic workspace to build and test applications. Prime examples are DigitalOcean, IBM SmartCloud, and CloudStack. **IaaS clients are like music companies that need to rent the recording studio, but bring all of their instruments, and vocalists, to record their music. They only need a stage.**

[According to Cloudfare.com](https://www.cloudflare.com/learning/cloud/what-is-the-cloud/), there is another common type of cloud service:
>Formerly, SaaS, PaaS, and IaaS were the three main models of cloud computing, and essentially all cloud services fit into one of these categories. However, in recent years a fourth model has emerged:
>
>Function-as-a-Service (FaaS): FaaS, also known as serverless computing, breaks cloud applications down into even smaller components that only run when they are needed. Imagine if it were possible to rent a house one little bit at a time: for instance, the tenant only pays for the dining room at dinner time, the bedroom while they are sleeping, the living room while they are watching TV, and when they are not using those rooms, they don't have to pay rent on them.
FaaS or serverless applications still run on servers, as do all these models of cloud computing. But they are called "serverless" because they do not run on dedicated machines and because the companies building the applications do not have to manage any servers.
>
> Also, serverless functions scale up or duplicate, as more people use the application — imagine if the tenant's dining room could expand on-demand when more people come over for dinner! Learn more about serverless computing (FaaS).

Now that we have an understanding of what the cloud is, how it works, and what it does, we can take a closer look at cloud architecture and how it could be attacked. Always remember two things: The first being that **The cloud is just someone else's computer.** and to always ask better questions.
