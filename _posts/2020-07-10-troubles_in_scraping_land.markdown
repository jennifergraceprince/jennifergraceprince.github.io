---
layout: post
title:      "Troubles in scraping land!"
date:       2020-07-10 15:01:40 -0400
permalink:  troubles_in_scraping_land
---



This where I will explain my CLI project for Flatiron School and talk about some of the issues I ran into while building my program.

I created the gem Learn About Dogs, a CLI program that scrapes a website to help the user learn about the characteristics of various dog breeds.

The idea was the user would type the command below to get started:

$ bin/learn-about-dogs

The user selects a dog type from the menu, either by typing a breed name or the menu number. Once the user has selected a breed, they would be able to select and view further details about the breed.


I used OpenURI to retrieve and return my chosen webpage's HTML as a string. Then used Nokogiri to parse. This was difficult to be honest, and I spent a lot of time reviewing the scraping lessons.

However, I ran into a ton of trouble trying to access the details page. Eventually, I realized that this was because there was javascript present on the dog breeds page which made it really difficult to drill down into the details pages the way that I wanted to.  I spent several hours trying to figure it out, and noticed the cats page was much shorter with no javascript present. So I changed my url to `/cats` and had a much easier time of things.  So I decided to change my entire program to "learning about cats", which involved changing many method names, file name, dependency names etc.  I sadly had to let go of the cute ASCII dog I made for the program as well lol.  
This was valuable - I learned a lesson about letting go and adapting to the situation when things aren't working as you had planned them out to.  I also learned that am not super stoked on the method of scraping websites for data this way, and if I had time to do it over again, I think I would have chosen an API.

I found planning out what I wanted my program to look like to be the easiest part.  I chose to simplify the information I displayed to just 4 categories per breed - a general description, history, personality, and grooming.  

I basically pulled two all-nighters and finally got everything working as I would like.  Then I spent time cleaning up the user interface.  

I tried to publish my program as a gem, but ran into issues.  At one point it was working (when it was still "learn-about-dogs"), but I eventually had to abandon the idea in the interest of time since it is not a requirement.

Overall, I am happy with my program and I learned excellent lessons about time management and scope.


