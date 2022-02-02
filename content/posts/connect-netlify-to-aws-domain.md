---
title: "Moving domain to Netlify from AWS Route 53"
date: 2022-01-31T11:10:36+08:00
draft: false
language: en
description: I had a website hosted on AWS. I built a `<weird-domain-name>`.netlify.app. I wanted to connect my stuff over. Reconfigure the DNS. It was quite simple but I'm assuming people are like me and look at blogs sometimes before docs.
keywords: ["AWS", "Netlify", "DNS", "domain", "Route 53"]
categories: ['How to']
tags: ['Tutorial', 'Netlify', 'Programming', 'DNS', 'AWS']
---

I had a website hosted on AWS. I built a `<weird-domain-name>`.netlify.app. I wanted to connect my stuff over. Reconfigure the DNS. It was quite simple but I'm assuming people are like me and look at blogs sometimes before docs. This guide is assuming you had a previous, functioning, www domain and apex domain setup.

---
## Summary

* Create an A name record in AWS
* Create a CNAME record in AWS
* Create a NS record in AWS
* Change your DNS 
* Change Name servers in Registered Domains
* Verify SSL in Netlify

---



{{< figure src="/assets/blog/connect-netlify-to-aws/getting-started.png" alt="Getting Started" >}}

Prerequisites:

* ```www.example.com``` 
* ```example.com ```
*  `<weird-domain-name>`.netlify.app

On Netlify go to your site. Then Site Settings > Domain Management. Add your domain alias. 
After which, check the DNS configuration. 


{{< figure src="/assets/blog/connect-netlify-to-aws/dns-config.png" alt="dns-config" title="dns-config" >}}

Copy these values. These are name server values.

In AWS go to route 53 > Hosted Zones > example.com

You want to delete all your prior records bar the record with the SOA type.

You're going to want to create a: 

* **CNAME** -> A Canonical Name record is a type of resource record in the Domain Name System that maps one domain name to another.
* NS -> A **DNS Name Server** (NS) record specifies the domain name of the name server servicing a particular domain.
* A -> The A-record or Address Record provides information about the IP address of your host / domain name.

The CNAME will map your www.example.com site to your `<weird-domain-name>`.netlify.app. 

The NS will view the custom bare site (example.com not www.example.com) as a record name. We pass in those name server values from Netlify, mentioned above.

The A record will be left blank so, the record name will be example.com and the value should point to an IP address. Namely, ```104.198.14.52```. That's the Netlify domain.

Your Route53 should look something like this. 

{{< figure src="/assets/blog/connect-netlify-to-aws/aws-records.png" alt="record-names" >}}

Going back your sites should look something like this.

{{< figure src="/assets/blog/connect-netlify-to-aws/custom-domains.png" alt="Custom domains" >}}

After which goto Registered Domains > example.com and edit the name servers with the values that netlify provide. Wait for it to propagate.

{{< figure src="/assets/blog/connect-netlify-to-aws/custom-dns.png" alt="Custom dns" >}}

Finally, go to HTTPS in the Domain management. Click Click Verify DNS Configuration. Wait 24 - 72 hours and in the meantime check your website progress on this [DNS checker](https://www.whatsmydns.net).

If it doesn't work try and diagnose with the commands below. 

And you're done.

### Troubleshooting bonus

```curl -s -v http://www.ibrahimsowunmi.com 2>&1 | grep -i server\n```

```curl -s -v http://ibrahimsowunmi.com 2>&1 | grep -i server\n```

The commands above ping your domain, it should say `netlify` somewhere in the content that is returned.

You can also use 

```host example.com``` 

```host ibrahimsowunmi.com```

To make sure they're routing correctly. The naked domain should return the Netlify IP address and your www domain should give the `<weird-domain-name>`.netlify.app. 

You can check your name servers with https://who.is/
Your apex and www domains are separate.

