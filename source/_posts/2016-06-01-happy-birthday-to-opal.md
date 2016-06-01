---
layout: post
title: "Happy Birthday to OPAL!"
date: 2016-06-01 16:00:55 +0000
comments: true
categories:
        - opal
author: David Miller
author_link: thatdavidmiller
image: assets/images/posts/birthday.jpg
---
Last Saturday 28th May 2016 marked the third birthday of OPAL - the
[Open Source framework](https://github.com/openhealthcare/opal) we created to help developers
create high quality clinical applications. We’ve come a long way since the
[very first commit back in 2013](https://github.com/openhealthcare/opal/commit/63917d2d288faca6201c65d0de6893a59577b75d)
so to celebrate we thought now would be a great time to take a look back over everything we’ve achieved.

## Early days

For the [first few months](https://github.com/openhealthcare/opal/graphs/contributors?from=2013-05-26&to=2013-07-02&type=c)
the lead developer on OPAL was the awesome
[Peter Inglesby](https://twitter.com/inglesp), who made that very first commit, and
worked with Drs
[Pollara](https://twitter.com/gpollara),
[Marks](https://github.com/michaeledwardmarks/) and
[Noursadeghi](https://twitter.com/mnoursad) to craft a Patient List system for infection patients at UCH. We met each
week in the old Library room at [HTD](http://www.thehtd.org/) for a show and tell and figured out what the next sprint would look like.

The interface changed almost weekly back then as we tried to figure out how best to replace the menagerie of Word
documents, T-Cards, Access databases and Excel spreadsheets that the teams were currently using as patient lists.
As you can see below, even three years on, the Patient List components of OPAL are still recognisable from those first few months!

<div class="post-thumb">
<center>
  <img class="img-responsive" src="/assets/images/posts/elcidopal.gif" />
</center>
</div>

## Making OPAL a Framework not an Application

Even at the beginning we knew that we wanted OPAL to be more of a framework than an application. By
[October 2013](https://github.com/openhealthcare/elcid/commit/b695828681b27e4b7932dd8eb0c70f5f9c55a8f1) we
started moving the UCH specific elements out of OPAL, refactoring it for reuse. We set about moving application specific
business logic into
[elCID](http://elcid.openhealthcare.org.uk) (the first OPAL application),
allowing OPAL to be the generic platform for the services we build.

OPAL would provide a sensible robust default configuration along with a
[core data model](http://opal.openhealthcare.org.uk/docs/v0.6.0/guides/datamodel/),
[reusable common components](http://opal.openhealthcare.org.uk/docs/v0.6.0/guides/components_overview/), UI
components, and a clear path for integration with other systems and standards. Meanwhile individual applications built with
OPAL would provide specialised domain logic for particular tasks, clinical specialties, or customisation for individual
installations.

## Deployment to an actual NHS Hospital

In January 2014 we were ready to deploy
[elCID](https://github.com/openhealthcare/elcid) to a real NHS hospital - just eight months after
starting the project. Since then it has been used to manage inpatients and outpatients for HTD and the Infection and
Microbiology teams at UCLH.

Digital services are never finished though - and we’ve
[iterated](http://openhealthcare.org.uk/blog/2016/02/16/how-were-helping-respond-to-the-zika-outbreak/) and
[improved](http://openhealthcare.org.uk/blog/2015/10/21/launching-a-new-walk-in-service/) both elCID and OPAL frequently. OPAL alone
has racked up 19 releases and almost 2,500 commits since we began. During that time we’ve worked to turn our vision for a
robust Open Source framework for building clinical web applications into a reality.

## Taking OPAL to NHS Hack Days

One of the big tests for how far along that path we are is how OPAL has performed as a tool for building projects at
[NHS Hack Days](http://nhshackday.com/). Hack days are a great way to stress test developer tools. They reward well-thought-out
APIs and good documentation,
giving you a great insight into how much they help or hinder developers.

The first OPAL project at a NHS Hack Day was back in
[May 2014](http://nhshackday.com/previous/events/2014/05/london/) when
[Dr Gabriele Pollara](https://twitter.com/gpollara) brought a team together to try and
add some extra features to OPAL and elCID. Even though the changes from
[their fork of OPAL](https://github.com/mastersplinter/opal) were never merged back into the
main codebase, it gave us plenty of insight into where we had the coupling wrong between framework and application, and
places where could improve the APIs or make the documentation clearer.

Four months later when the 8th NHS Hack day rolled around in
[Leeds](http://nhshackday.com/previous/events/2014/09/leeds/) the codebase had improved significantly - with a project
to design a
[handover tool for Renal teams](https://github.com/openhealthcare/opal-renal) coming joint first:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Renal project team collect T shirts for coming joint first at <a href="https://twitter.com/hashtag/nhshd?src=hash">#nhshd</a> <a href="http://t.co/D6EUkAUDdg">pic.twitter.com/D6EUkAUDdg</a></p>&mdash; Alison Cameron (@allyc375) <a href="https://twitter.com/allyc375/status/516225627423518720">September 28, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

This was the first time we had built a brand new application from scratch using OPAL, and it gave us a clear head
start over hackday projects that had had to start from nothing.

Over the next year, projects like
[eCDR](https://github.com/TeamBigPharma/bigpharma) and
[travelalerts](https://github.com/nhshackday/opal-travelalerts) were a great benchmark of how OPAL was progressing. New developers
were able to get to grips with it and start building on top of it over the course of just a weekend. The framework was
obviously maturing.

In the most recent London NHS Hack Day we saw two projects building on top of OPAL - A
[digital anaesthetic chart](https://github.com/anaesthetic-health-chart) that pulls
and displays observation data from a anaesthetic monitors, and the eventual winner - a
[Raspberry Pi based EPR in a box](http://github.com/nhshackday/outbreak).

<center>
<div class="post-thumb">
<img class="img-responsive" src="/assets/images/posts/dacer.png" />
</div>

<iframe width="560" height="315" src="https://www.youtube.com/embed/hJWTpSH8Bxc?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>
</center>

It was particularly exciting to see two brand new - and completely re-skinned OPAL projects built over one weekend and to
get lots of feedback from all of our friends in the NHS Hack Day community.

## The last few months

The [last few months](https://github.com/openhealthcare/opal/graphs/contributors?from=2015-07-22&to=2016-05-28&type=c)
have seen OPAL leap forward in terms of
[code quality](https://coveralls.io/github/openhealthcare/opal) and depth of features. In large part this is thanks to the hard work of
[Fred Kingham](https://twitter.com/fredkingham) - who has taken over as lead developer for the project. The upcoming
[0.6 release](http://opal.openhealthcare.org.uk/docs/v0.6.0/) will see many improvements. We’ve refactored form helpers to make it easy to embed forms. Added new Patient detail views and a new Patient List module to make OPAL even more customisable. We’ve also added in an integration layer for connecting to other hospital systems. All this coupled with even greater performance.

We’re not done yet though! We’re looking forward to improving the
[documentation](http://opal.openhealthcare.org.uk/docs/v0.6.0/) to make it easier for new developers, we’re updating our core clinical models, improving the way in which we guide users through complex clinical pathways, adding further UI improvements for mobile devices along with much more as we move towards a 1.0 release.

If you want to know more about OPAL, or about the work that we do at Open Health Care building digital tools for clinicians,
[drop us a line](mailto:hello@openhealthcare.org.uk) - we’d love to hear from you.

<small>
Photo credits: [Will Clayton](https://www.flickr.com/photos/spool32/)
</small>
