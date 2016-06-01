---
layout: post
title: "Launching a new Clinical Digital Service for returning travellers"
date: 2015-10-21 20:00:29 +0000
comments: false
categories:
        - opal
        - elcid
author: David Miller
author_link: thatdavidmiller
image: assets/images/posts/htd.jpg
---
Just a couple of weeks ago we launched a new service at the [Hospital for Tropical Diseases](http://www.thehtd.org/home.aspx)
in London to help the doctors and nurses who run their [Emergency Walk-In Clinic](http://www.thehtd.org/emergencies.aspx).
At the clinic,
travellers who have returned from the tropics and are acutely unwell turn up without requiring an appointment to get treated
by specialists in tropical diseases. The service tracks patients on their journey through the clinic, from initial triage to
following up on lab results that arrive after they've left.


<div class="post-thumb">
  <img class="img-responsive" src="/assets/images/posts/walkin.referral.png" alt="" style="border: 2px solid black;" />
</div><!--//post-thumb-->

We worked closely with the staff who run the clinic, making sure that we met the different needs of different types of user
- in this case admin staff, the nursing staff, doctors, as well as the service managers who wanted data on what activity was
happening. Just like we do with all of our services, we brought them into our agile development process as we iteratively
developed the service based on research and their feedback.

Clinical digital services too often fail to take into account the experiences of the people on the ground who have to use
them in practice. At Open Health Care we don't think that's acceptable for something as important as delivering health care.

Because of that we will continue to regularly meet with users of the service to conduct usability testing and actively seek
feedback so that we can continuously improve the service. That feedback loop needs to be a part of the ongoing operation of
digital products and services in hospitals - not just something that happens as part of an initial design phase - and we've
seen before just how useful it can be as we've been able to respond to changing user needs and changes to the context and
processes that surround users experiences of our services.


<div class="post-thumb">
  <img class="img-responsive" src="/assets/images/posts/walkin.nurseledcare.png" alt="" style="border: 2px solid black;" />
</div><!--//post-thumb-->

<h2>Use data to design services.<br>It makes things better</h2>

One of the key goals of the project was to allow the team at HTD to gather high quality data about the cohort of patients
that they treat. This data is hugely valuable, both academically for research purposes, and because it enables the team
to understand their workload.

When the tools that are used for routine day-to-day clinical care don't collect usable data, the cost of analysing what you've
been doing become huge. With the new Walk-in service however, all of the information that the institution knows about a patient,
from demographics to observations, travel history to treatment, gets stored as high quality structured data.

That means that anyone can get an accurate answer to a question like "How many patients did we see with Dengue fever in the last
year" in seconds, rather than it taking hours or days of painstaking work reviewing case notes, or manually curating and maintaining
their own databases.

We're excited about the possibilities for service redesign and research that this new capability has opened up for the team, and
we've already been brainstorming ideas - so watch this space!

## How it all came together

The service was built as a [plugin](https://github.com/openhealthcare/opal-walk-in) for [OPAL](http://opal.openhealthcare.org.uk) -
our open source framework for building high quality digital services in a clinical setting, and is deployed as part of
[elCID - an existing service that we run for UCLH](http://elcid.openhealthcare.org.uk) to manage patients with infection.

We love delivering high quality digital services for doctors.
If you'd like to explore how we might be able to help you out at your
institution, [get in touch](http://openhealthcare.org.uk/contact.html) - we're always keen to meet people with interesting problems
to solve as we try and make sure that the digital services that clinical staff in the NHS use in their day jobs is as good as the
services they use in their personal lives.


<div class="post-thumb">
  <img class="img-responsive" src="/assets/images/posts/walkin.advice.png" alt="" style="border: 2px solid black;" />
</div><!--//post-thumb-->
