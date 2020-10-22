---
title: "Tracstock"
collection: portfolio
created: July-August 2020
order: 1080
---
Tracstock is a website for tracking stocks and notifying users when their selected stocks reached certain conditions (i.e. stock price was less than, greater than, or equal to an amount set by the user). Users would add stocks to track and their desired conditions for receiving a notification. For example, a user would add Apple stock and set the condition for receiving the notification to price is greater than \$100.00. When the stock price exceeds \$100.00, the user would be notified. 

The website was built using C#, AS.NET Core, Entity Framework (a framework for accessing and manipulting databases through code), JavaScript, and HTML. The website was planned to be a subscription service, so the PayPal payments system is integrated. 

I purchased a domain and a server for the website, and set-up all the hosting software. The website worked and was accessible through the internet. Unfortunately, I did not continue hosting the website because of time commitments. 


{% capture fig_img %}
![Home page of Tracstock website]({{ "/images/portfolio/tracstock_home_page.png" | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Home page of Tracstock website</figcaption>
</figure>
