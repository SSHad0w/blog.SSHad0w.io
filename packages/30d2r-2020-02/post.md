---
layout: post
title: "30D2R - February: Web Application Basics"
date: 2020-06-04
categories: ['30D2R']
---
This post is a part of my [30 Days 2 Root](https://dev.to/sshad0w/30-days-to-root-challenge-introduction-3idp) challenge series.
Essentially, I am trying to learn the basics of a different facet of cybersecurity each month. [Click here](https://dev.to/sshad0w/30-days-to-root-challenge-introduction-3idp) to learn about how the challenge works, or tell me what I should study next!

Nowadays, every organization needs a website to reach further audiences. Businesses need more people to see their product, nonprofits need a place to accept donations, and schools and governments can register people in their systems without having to wait in long lines. Websites and apps have become the cornerstone of our society. We order products and services on them, we trust they're they __only__ ones with our private information like passwords or [PII](https://www.google.com/search?&q=define+pii) that could allow someone steal your identity, and we sometimes give them access to our cameras, microphone and contacts to enable full functionality. 


What would happen if an attacker could access **_all_** of this? 

This is why organizations need their WebApp assets tested. To ensure the privacy and safety of their users. Needless to say, this skill is in _extremely_ high demand in the age of websites being the point of contact and point of sale for most companies. 

Before I learned how to attack websites, I needed to know how they worked. So today, we will explore how websites work. This knowledge helped me understand the basics of Bug Bounty (Which I will cover in the next post) 

Every time a user interacts with a WebApp, the application, API, or browser (also known as the "Client") contacts the server and makes a request. This request is then sent to the server and the server reads the request and sends the client a response back. The information in the request and response may only be text, but this text is interpreted into the websites and apps we know and love. 


### **What is a request?**

A web request is the message that goes from your browser to the web server. It's called a "request" because it "requests" information from the web server. 

These are the standard parts of an HTTP request.

![Alt Text](/assets/img/30d2r-2020-02/img_81c551c03265.png)

These are the most common parts of a request:

#### The method
Each individual request does an action known as a method. These are the most common methods:
![Alt Text](/assets/img/30d2r-2020-02/img_f198ff493a61.png)

For security reasons, these methods aren't always allowed, as they can be used to exploit security holes in the server's infrastructure.

#### The headers
![Alt Text](/assets/img/30d2r-2020-02/img_694554a3dd4b.png)

The headers mostly tell the server information about the client, and data about the message itself. This metadata is part of what preserves the integrity and ensures the security of the message.



#### The body
The body can contain whatever information the user is trying to submit to the server. For example, if the server has three files on it and the method of the request is "DELETE", the server needs to know which file to delete. This type of information is stored in the body of the request. 

#### The Cookie

You've probably seen messages like this on some of your favorite websites, but what do they mean?

![Alt Text](/assets/img/30d2r-2020-02/img_8dc9560054eb.png)

A cookie is a personal identifier that is given to each site visitor that basically tells the server who is who. Cookies are primarily for websites to remember things like what you've already browsed, or information that helps advertisers. Without unique identification, the website may not be able to tell who is who, and one person may be able to hijack the session of another user. There are alternatives to cookies, like JSON web tokens, and other things, but they are all essentially used to identify sessions. 

[A short video on the basic parts of a request](https://www.youtube.com/watch?v=pHFWGN-upGM)

### **What is a response?**

After the client sends the request to the server, the server gives a response.

A typical response has the following elements.

#### A Status-line

When the server gives back a response, it responds with a status code. This code indicates the state of the response. 

![Alt Text](/assets/img/30d2r-2020-02/img_41209622e112.gif)

If you look at the photo, you see that there's a clear pattern. if the response has a status code that that starts with a:

* 2; The response is a success! If there is content on the page, you should see it loading.
* 3; The page you requested works, but it's redirecting you to another.
* 4; Client error. Something on your side isn't working.
* 5; Server error. Something on the server side isn't working.


So if the response status code begins with a 2 or 3, everything works. However, if the response code starts with a 4 or 5, there is some sort of error.  

#### Header information

![Alt Text](/assets/img/30d2r-2020-02/img_cc7099e60414.png)

This type of information can vary in many ways. This tells more about the connection and website itself.

#### The body

The body typically holds the actual HTML in the webpage, sometimes JavaScript and pretty much anything else that the page returns.

[Here is a much more in depth look at responses](https://www.tutorialspoint.com/http/http_responses.htm)

### **What is URL encoding?**

If you've ever used a terminal, or any programming language, you understand that there are two different types of characters. There are readable characters __like these__ and there are "special" characters like "!@#$%^&*()" and more. These types of characters are used in the computers native language, which is why no one can create a filename with a "/" in it. In Linux systems, that character represents a new directory. 

People put these types of special characters in articles, headers, or other parts of text that end up in the link. The machine that reads the link cannot tell the difference between a "+" put in the name of the article and the + in the native language, so it translates that character to text that the machine reads and translates back without executing any undesired characters.

As an example, search "Hello" on google and observe the link. 
Then search "+" on google and observe how there is no "+" in the link. It will have been translated to "%2B".

How do I know what it will be encoded to? Each character has its own translation, and there are many translators online that can encode and decode characters. 

These characters are in the requests so the server understands them, and are automatically decoded back in the response.

### **Subdomains**

A subdomain in simply another website that the organization owns that is attached to the root domain. A subdomain can look like a few different things.

Google.com (root domain)
Google.com/docs (subdomain)
Mail.google.com (_also_ a subdomain)

Sometimes companies will spend more resources in protecting and securing the assets on the parent domain and neglect the subdomains. This is why lots of website testers like to enumerate the subdomains to test each domain's security posture. 


Even though there are many other facets that make websites tick, these are the absolute basics that everyone in security should understand. This foundation is also critical for everyone who wants to break into bug bounty, which I will show in my next post.