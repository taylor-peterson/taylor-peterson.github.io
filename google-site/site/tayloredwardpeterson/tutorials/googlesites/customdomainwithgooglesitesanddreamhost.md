

---
layout: page
title: Custom Domain with Google Sites and DreamHost
---

  

| 
  

 | 
 I had an inordinate number of struggles getting a custom domain set up with Google Sites and DreamHost. This was only exacerbated by the lack of comprehensible resources on the issue. To save myself and others from this in the future, I present the following steps: 
  

1. Make a Google Site 
2. [Go buy a domain from DreamHost.](http://www.dreamhost.com/domains/)
3. Prep your domain for mapping your Google Site 
  1. Click on "Domains" -\> "Manage Domains" in the left panel 
  2. Click on "Edit" under "Web Hosting"  
  3. Unpark your domain (bottom of page) 
  4. Click on "Host DNS only!" 
  5. Go back to "Manage Domains" 
  6. Click on "DNS" 
  7. Add a CNAME record to your DNS configuration: 
    - Name = www
    - Value = ghs.googlehosted.com)
4. [Verify your domain with Google's Webmaster Tools](https://www.google.com/webmasters/tools)
  1. Click "Add a site" 
  2. Type in the URL of your DreamHost domain (including www.) 
  3. Click "Continue" 
  4. Select "Other" from the drop down menu 
  5. Head over to DreamHost 
  6. Add the indicated TXT record to your DNS configuration: 
    - Leave "Name" blank 
    - Enter the string Google gave you as the "Value" 
  7. Click "Verify" when you're done (this may take a few minutes) 
5. Map your Google Site to your new domain 
  1. Head on over to the "Manage Site" Page 
  2. Click on "Web Address" in the navigation bar on the left 
  3. Type your web address into the bar (include "www.") and click Add 
  4. You should see your web address pop up as "Canonical". This means that this is the address which Google will index.Â 
6. That's it! Now just wait a while (e.g. 12 hours) for the gears to churn and set things up. Soon enough, your custom domain will display your Google Site.  
7. Email tech-support to setup up a naked-url redirect.Â 

 | 
  

 |

  

