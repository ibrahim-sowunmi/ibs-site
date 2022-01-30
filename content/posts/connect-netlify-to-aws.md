---
title: "Moving domain to Netlify from AWS Route 53"
date: 2022-01-30T11:10:36+08:00
draft: false
language: en
description: I had a website hosted on AWS. I built a `<weird-domain-name>`.netlify.app. I wanted to connect my stuff over. Reconfigure the DNS. It was quite simple but I'm assuming people are like me and look at blogs sometimes before docs.
---

I had a website hosted on AWS. I built a `<weird-domain-name>`.netlify.app. I wanted to connect my stuff over. Reconfigure the DNS. It was quite simple but I'm assuming people are like me and look at blogs sometimes before docs.

{{< figure src="/assets/blog/connect-netlify-to-aws/getting-started.png" alt="Getting Started" >}}

Prerequisites:

* ```www.example.com``` 
* ```example.com ```
*  `<weird-domain-name>`.netlify.app

On Netlify go to your site. Then Site Settings > Domain Management. Add your domain alias. 
After which Check the DNS configuration . 


{{< figure src="/assets/blog/connect-netlify-to-aws/dns-config.png" alt="dns-config" title="dns-config" >}}

Copy these values. These are name server values.

In AWS go to route 53 > Hosted Zones > example.com

You want to delete all your prior records bar the record with the SOA type.

You're going to want to create a: 

* **CNAME** -> A Canonical Name record is a type of resource record in the Domain Name System that maps one domain name to another.
* NS -> A **DNS Name Server** (NS) record specifies the domain name of the name server servicing a particular domain.

The CNAME will map your www.example.com site to your `<weird-domain-name>`.netlify.app. 

The NS will view the custom bare site (example.com not www.example.com) as a record name. We pass in those name server values from Netlify, mentioned above.

Your Route53 should look something like this. 

{{< figure src="/assets/blog/connect-netlify-to-aws/aws-records.png" alt="record-names" >}}

Going back your sites should look something like this.

{{< figure src="/assets/blog/connect-netlify-to-aws/custom-domains.png" alt="Custom domains" >}}

Finally, go to HTTPS in the Domain management. Click Click Verify DNS Configuration.

And you're done.
