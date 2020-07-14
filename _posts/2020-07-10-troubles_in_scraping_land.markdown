---
layout: post
title:      "Learn About Cats CLI Project"
date:       2020-07-10 15:01:40 -0400
permalink:  troubles_in_scraping_land
---



This where I will explain my CLI project for Flatiron School.

For my project I created a program titled Learn About Cats, that scrapes a website to help the user learn about the characteristics of various cat breeds and presents the information in an organized, digestible way.  The program uses Open-URI and Nokogiri to scrape and parse the page holding the list of all breeds, as well as the individual breed pages.

The idea was the user would type the command below to get started:

$ bin/learn-about-cats

And then arrive at a menu showing a welcome menu, initial list of 10 breeds, and navigation options.

Here is a 15-second giphy demo to give you an idea of my program:

<iframe src="https://giphy.com/embed/dry8LD0cbTS5B2HKZm" width="480" height="349" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/dry8LD0cbTS5B2HKZm">via GIPHY</a></p>

From this view, the user can navigate through a broken-out list of 10 breeds at a time, or view all breeds at once.

The user may select a breed either by typing it's name, or corresponding menu number.  I used the .downcase method to make sure the user's entry would not be case-sensitive.

When the user has selected a breed, the user will then arrive at a submenu for that specific breed.  The submenu will contain a breed title, as well as 4 information selections to choose from - Description, History, Personality, and Grooming. Using the same navigational format, the user can choose any of these four options to view the information text from that section of the individual breed's page.  They will also arrive at a third submenu, which will allow them two options - to go one level up back to the breed's individual submenu, or to return to the main menu and view all breeds.

There is more information available on the breed page itself, such as "Health", "Finding", and a breed rating, so there is a fifth option, "View On Web", that allows the user to actually open the breed's individual web page from the command line.  This option gives a message in the terminal that the user's web browser is opening, as well as the option to continue using the program by staying on the submenu or navigating back to the main menu.

The user can type "exit" at any point in the program to leave the program.

I really enjoyed building this program overall.  I ran into some challenges along the way.  

During my first review, I received feedback on how to improve my program.  

I fixed an edge bug in my program where hitting `next` twice at the end of the breed list caused a fatal error.  I had set my instance variable for the index of my list of breeds at too high a value.  This was because my program was originally pulling 243 dog breeds.  So I set it to 49 in all areas where the @d variable appears in my code, to account for 50 cat breeds (since counting starts at 0).  This resolved the `next next` bug.

The reviewer also suggested it might be nice to have an option to open the breed's webpage URL.
I opened a test throwaway branch, and experimented with a few options.  I first tried a gem called "watir", but it threw me an error that indicated it would like me to use selenium webdriver as well. I bookmarked two other options, Launchy and Mechanize.  Launchy was what I tried first and ended up working, so I went back to my master branch and worked that feature into my program.  The reason I did not create a PR and merge from my test branch is that on my test branch I implmented the option on the sub-sub-menu, and I decided I'd rather keep it at the general breed submenu. Additionally, my branches had fallen out of sync because of the color changes I'd made on master. So rather than deal with a rebase, I just went back to master and started fresh.  However in a real world situation, I would have rebased against master, resolved any merge conflicts, and then opened a PR and merged my test branch into the master branch.

I also decided I wanted to make my program look nicer, and decided to add the colorize gem.  I had a lot of fun spicing up the look and feel of my program, adding an ASCII cat, blinking message, and a blinking mouse running away from the cat.  I almost made a mistake here, as I use a white background on my terminal window, and got caught up and specifying some text as black.  Then I realized that many people use black background for terminal, so I corrected my code to ensure text would not be rendered invisible on another user's local environment.

I also struggled with the challenge of really time management, which is an important component of programming.  Due to circumstances beyond my control, I ended up beginning this project far too late. Because I did not take time for the planning process, I lost an evening trying out various project ideas.  In the future I would make sure to give adequate respect to the planning process to avoid stress.  I would liked to have spent more time bundling my project as a gem.  I also initially wanted to include dogs or both dogs and cats, but that proved to be too challenging.  I settled on dogs, and ran into challenges at a late hour and eventually changed the entire program to be cats.  The dogs breed page contained javascript elements with interefered with my scraping code.  I learned from my instructor that when conditional javascript is present on a webpage, it can interfere with scraping to the point where it's less likely you will be successful.  I think in the future I will seek to use APIs to avoid similar issues.  This was valuable - I learned a lesson about letting go and adapting to the situation when things aren't working as you had planned them out to.


Another issue I ran into, is actually one that I've been actively working on at my day job as well where I work as a QA Engineer.  I am often able to figure out code and write automation code, but I struggle with articulating abstract concepts verbally.  I am from a creative background and primarily a visual learner/learn by doing type - probably why the UI portion of my program was my favorite - and I struggled being "on the spot" this during my review, my brain kind of freezes up and the words don't always come.  I made sure to review abstract concepts prior to my second review so that hopefully I may explain them better and better demonstrate my understanding of the material.

I'm actually glad that I failed my first review because I gained a lot of knowledge by having a second go and refactoring my program, and better internalized the concepts we've learned so far in studying Ruby.

During my second review, we went over some refactoring and live coding. I realize I can improve my ability to perform live coding by joining more study groups.

Overall I really enjoyed this experience.  




















