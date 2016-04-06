---
layout: post
title: "How we manage risk when we use open source in health"
date: 2016-04-06 08:00:29 +0000
comments: false
categories:
author: David Miller
author_link: thatdavidmiller
image: assets/images/posts/some.code.jpg
---
In the last couple weeks, many thousands of words have been written about a small piece of open source code called left-pad which was suddenly un-published by its author. (If you’re not up to speed on this, then you might like to
read a [narrative overview](http://www.theregister.co.uk/2016/03/23/npm_left_pad_chaos/), or
[some](http://www.haneycodes.net/npm-left-pad-have-we-forgotten-how-to-program/)
[interesting](http://lucumr.pocoo.org/2016/3/24/open-source-trust-scaling/)
[analysis](http://blog.npmjs.org/post/141577284765/kik-left-pad-and-npm).)

Perfectly understandably, this has caused lots of people to re-consider the risks of building on open source, and how the actions of unaccountable external developers halfway around the world could have an effect on how your software operates.

When we work with digital tools for health, risk can be particularly profound. The failure mode of a digital service that supports clinicians delivering direct care is the risk of IT failures causing harm to patients, not just a website being unavailable for a while. This means that we need to make sure that our attitude to risk is appropriate to the harm that failures can cause.

Thankfully, there are plenty of people using open source, and lots of them using it for mission critical applications that have exacting uptime expectations. That means that the path to processes and tools to mitigate these risks is well trodden, and we can learn from the wealth of cultural knowledge in the open source movement.

Taking a straw poll of the table I'm sat at, there are people who've written code using open source for investment banks, power stations, government departments, and yes, NHS hospitals.

The story of how all those places avoid their production systems being broken by code that has been altered by unknown open source developers is basically identical.

### Software Dependencies at Open Health Care


<div class="post-thumb">
  <img class="img-responsive" src="/assets/images/people/david.ross.jpg" alt="" />
</div><!--//post-thumb-->


A <a href="https://en.wikipedia.org/wiki/Coupling_(computer_programming)">dependency</a> is a
broad software engineering term used to explain the relationship when a piece of software relies
on another one. When programmers install and run software from other sources, they will most often use a
[package manager](https://en.wikipedia.org/wiki/Package_manager) - software that automates the
process of installing and upgrading code.

Before we install a new package or module of open source code, we carefully evaluate it. We look at the code, we look at its user base, we look at how actively maintained it is by the open source community and we look at the risk that it presents to the rest of our code base. The decision has to be signed off by at least two people in our development team, and it’s not one we take lightly. (Explaining how this review and evaluation process works in detail is probably a whole post in itself.)

Once we’ve taken that decision, we have to update our code to incorporate the new dependency.
[Every](https://pypi.python.org/pypi/)
[major](https://www.npmjs.com/)
[open](https://hex.pm/)
[source](https://rubygems.org/)
[package](http://www.cpan.org/)
[manager](https://help.ubuntu.com/lts/serverguide/package-management.html) includes the concept of
[software versions](https://en.wikipedia.org/wiki/Software_versioning). When we use external code, we "pin" that code to
[a particular version](https://github.com/openhealthcare/elcid/blob/v0.6.0/requirements.txt). The exact mechanism we use to do that varies, but always means that we end up explicitly defining the exact version number of a piece of code in our application.

That means that every time we re-install, we get the exact same software.
Our [automated test suites](https://travis-ci.org/openhealthcare/) are run against the exact same software. When we deploy to a staging environment to do testing and quality control, it's the exact same software. When we deploy to production... you get the picture I'm sure.

If the author of that code releases a new version, we’ll hear about it from the project mailing list, or from blog posts about it, but that code doesn’t automatically find its way into our applications.

When we decide to upgrade a dependency that's a task that's
[assigned to a programmer](https://waffle.io/openhealthcare/opal-ideas) as part of a
<a href="https://en.wikipedia.org/wiki/Scrum_(software_development)#Sprint">sprint</a>. That task
will consist of a number of things:

* They have to review the changes to the library.
* They have to change several pieces of configuration management code.
* They have to run all of our automated test suites and make sure they pass.
* They have to get the upgrade accepted by a [peer review process](https://help.github.com/articles/using-pull-requests/) (another programmer has to OK the decision).

And that's just to change the latest version for a fresh install. It is nowhere near production yet. To get there you have full change approval and acceptance testing processes that are in place for
individual deployments.

### So how did left-pad affect us?

The short answer is, it didn’t.

By the time the applications we support are deployed, they safely include all of the code that’s required to run them, and that code is carefully managed.

The real disruption caused by left-pad was to the working life of programmers. It would have meant that new installations failed, or
perhaps [automated test suites](https://en.wikipedia.org/wiki/Continuous_integration) didn't pass. If we’d been working at 22:30 PM last tuesday, then during the two and a half hours that the whole affair lasted, it might have made us a little less productive. If we’d been doing a planned upgrade or deployment of one of our applications, we might have had to postpone it. (Although we likely would have been just fine with the specific left-pad issues.)

What it has meant, is that we’ve taken the opportunity to review our processes to make sure that we’re following established best practices for open source development in domains where managing risk is as important as health. And we welcome that opportunity - we’re always striving to make sure that our engineering standards are as high as possible.

## Open Source or just good software engineering?

One of the great things about the open source movement is that we’re able to have high quality conversations about things like risk and failure in the open. When things go wrong, we’re happy to talk about it. The open movement shares its knowledge from the tough times as well as the good times. The open movement means that the stakeholder involvement and the responsibility is shared. If a solution needs to be found, it can often be found quicker and to a higher standard because it is being required and reviewed by such a large body of individuals.

More broadly, every software vendor, produces applications that depend on code they haven’t written themselves - regardless of licensing. Managing dependencies is a part of all modern software engineering. The most important factor here is not the licence under which that code exists. What does matter, is having an approach to risk that’s appropriate and responsible.

If you’d like to know more about the processes we use to make sure that we deliver the highest quality service to the clinical teams who use our products,
or if you’d like to know more about how we might be able to help you, then do <a href="mailto:hello@openhealthcare.org.uk">get in touch</a>.

<small>
Photo credits: [Paul Clarke](flickr.com/photos/paul_clarke/)
</small>
