---
layout: post
title: "My own .info domain"
date: 2011-11-26 02:34
comments: true
categories: blog github DNS
---


Today I had a day off after a looooong day of traffic jams and a gig
at the [Odeon](http://www.odeondespiegel.nl/home) theater in Zwolle.
Anyway having a day off does not mean no sitting behind the computer.
On the contrary, now that I have the time let's start hacking.

### Github

First I started organizing my github projects. Some searching pointed
me in the direction of _Organizations_. A useful concept and it fitted
nicely with my plan of creating accounts per customer. So I created
some gmail accounts, one for each customer and then created parallel
accounts on github. Finally I moved the projects to the correct
organization.

### Personal domain

Secondly I decided that it would be a cool idea to have a personal
domain point to my [github blog](http://zetafish.github.com/) And what
I need for that is first a domain.

I registered the `endymionkasanardjo.nl` domain on
[eksolutions.eu](http://eksolutions.eu) which seemed a sweet deal with
just 5 EURO for a year. However I did not immediately see how to setup
the forwarding. It turned out that forwarding costs an additional 2.40
EURO.

Enter [godaddy](http://www.godadday.com/). They offer a .info domain
for 
only 1.6 EURO a year. And what is more full access to DNS record
to manage forwarding myself.
[Here](http://www.google.com/support/blogger/bin/answer.py?hl=en&answer=58317&topic=12451)
I found out how to set up the CNAME record with godaddy.

Next I set up the CNAME file for my github blog. So that github knows
what to do when someone thinks they are talking to the
endymionkasanardjo.info domain
    
    echo endymionkasanardjo.info >> source/CNAME
    rake generate
    rake deploy
    
Yipeeeee. I am fully online now, and you can visit me on [http://endymionkasanardjo.info/](http://endymionkasanardjo.info/)

