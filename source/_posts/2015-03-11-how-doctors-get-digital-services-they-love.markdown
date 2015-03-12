---
layout: post
title: "How Doctors get digital services they love"
date: 2015-03-11 21:12:19 +0000
comments: false
categories: 
author: David
author_link: thatdavidmiller
image: assets/images/posts/userstories.jpg
---

At Open Health Care, we believe in
[User-centered design](https://www.gov.uk/service-manual/user-centred-design).

Which means that we focus on meeting the needs of our users, and is why we
always work in close collaboration with them. Whether that comes in the 
form of making sure that our clinical champions are present at every sprint 
meeting, or working hard to get clinical staff and patients along to
[NHS Hack Day](http://nhshackday.com) we work by putting users first, building
and testing in small chunks.

Working this way means that generally when we work on a project, we identify 
clinical champion(s) for that project. These are the kind of people who will use the service
we end up building in their day-to-day work. In order to get them as involved as
possible, we introduce them to [Agile](https://www.gov.uk/service-manual/agile), 
and we often find ourselves teaching [doctors](https://github.com/GabPoll) to 
[github](https://github.com/michaeledwardmarks). (Yes, that's a verb now).

The great thing about working in multidisciplinary teams, is that *everyone* learns
new things, all the time. For every medical three letter acronym like say, 
[CAP](http://en.wikipedia.org/wiki/Community-acquired_pneumonia) that gets explained 
to a developer, there's an explanation of what 
[API](http://en.wikipedia.org/wiki/Application_programming_interface) stands for that goes the
other way.

But it's not just terminology that gets shared - often we try to share our tools. We
promote online 
[collaborative](http://www.google.co.uk/docs/about/) 
[document](http://hackpad.com/) editing above email attachments and
[naming conventions](http://thedoghousediaries.com/5964). We encourage users to take 
up better web browsers. We get them to try out modern
[team communication](https://slack.com/) [tools](http://appear.in), and recommend [Open Source](http://www.rstudio.com/)
alternatives to the proprietary default incumbents.

### But wait - it gets better

Not only does this help us all understand one another better, which is so vital to delivering 
high quality digital services, but it also often introduces clinicians to tools that reward 
power users with advanced functionality. Once you've learnt
[markdown](https://help.github.com/articles/github-flavored-markdown/) once, typing information
into text boxes that will get rendered in a web browser is never quite the same again. You start 
*expecting* that the web based [clinical digital services](http://opal.openhealthcare.org.uk) 
you use in your day job let you [use markdown](https://github.com/openhealthcare/opal/blob/823de649ddee6c13803264d929ece3ae171104c5/opal/static/js/opal/opaldown.js)
there too.

Possibly the best feature we've implemented that came about this way is the 
[OPAL ](http://opal.openhealthcare.org.uk)
Macros from 
late last year. Directly inspired by [Github issue mentions](https://github.com/blog/957-introducing-issue-mentions),
OPAL Macros let the user define blocks of commonly used text, and then insert them with shortcut Macros - 
(names preceded by the # symbol). 

For instance, for [Staph](http://en.wikipedia.org/wiki/Staphylococcus_aureus) advice, the user enters #st: 

<img class="img-responsive" src="/assets/images/features/macro.pre.png" alt="" />

... which then expands to the (institutionally defined) standard advice for this case: 

<img class="img-responsive" src="/assets/images/features/macro.post.png" alt="" />

This is the kind of user need that only even comes up when users are digitally literate enough to
be able to express it - something along the lines of:

<blockquote class="custom-quote"><p><i class="fa fa-user-md fa-3x"></i>
As a Doctor <br />
I want to avoid repeatedly typing out standard advice <br />
So that I can spend more time with my patients
</p></blockquote>

The existence of this kind of power-user functionality encourages users to master their tools, by
offering them time savings and efficiencies but crucially, doesn't interfere with the user experience at all if you 
don't know it's there. As
[Dr Marks](https://github.com/michaeledwardmarks), who had originally explained the need on
Github said:

<blockquote class="custom-quote"><p><i class="fa fa-quote-left"></i>
Absolutely stunning.<br/>
I would say this is one of the most incredible things I have seen on a piece of NHS software ever.
</p></blockquote>

If you're interested in starting an OPAL project at your institution to take advantage of this kind 
of feature, or in seeing how we can can help you by providing clinical facing digital services,
don't hesitate to [Get in touch](/contact.html)!

<small>
Photo credits: <br />
[Jacopo Romei](http://www.flickr.com/photos/jakuza/)<br />
</small>
