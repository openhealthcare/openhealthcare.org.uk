---
layout: post
title: "Big problems in health tech that get us excited"
date: 2016-06-06 11:59:20 +0000
comments: true
categories: ohc
author: David Miller
author_link: thatdavidmiller
image: assets/images/posts/nhshd9.diagram.jpg
---
One of the great things about working in health is that there are no shortage of exciting, and potentially impactful problems to
work on. At Open Health Care, we spend a lot of our time working to ease a couple of the big headaches around usability and
data that the current state of health care technology gives clinicians.

## Usability

First is the usability problem.

We’re hardly the first people to suggest that many, if not most of the digital tools that are provided for doctors, nurses and
other key front line NHS staff struggle with usability. By default these tools tend to be overwhelming and unfriendly. They are
hard to use, and at times downright dangerous.

At Open Health Care we believe that medicine is important enough to deserve the very best in terms of high quality usable software.
In an environment where the costs of making mistakes is so high, clinicians deserve tools that help rather than hinder.

The great thing is that technologists understand how to make tools that are highly functional and even delight their users. It
requires time, focus and a willingness to change the way things are done - but the
[design](http://thisisservicedesignthinking.com/)
[and](http://www.usability.gov/what-and-why/user-centered-design.html)
[development](http://www.agilemanifesto.org/)
[techniques](https://www.gov.uk/service-manual) are
increasingly widespread and available to us.

There is no reason why we can’t do this for medicine - and indeed, the biggest part of what we do as Open Health Care is
[delivering that](http://openhealthcare.org.uk/blog/2016/02/16/how-were-helping-respond-to-the-zika-outbreak/).

In the UK, our reality is that we are looking to streamline and improve the efficiency of our clinical services in the name of yes,
better care but also saving the NHS money. Having usable digital tools that genuinely support the day to day work of those services
with the capability to be frequently iterated will be a key plank of any successful transformation strategy as we look to re-design
those services.

## Data

The second big area that gets us excited is clinical data.

If we get sick, then the people and institutions who care for us know a huge amount about us. But that information is rarely
available as data. It’s either literally on paper notes, or it’s in electronic systems that may as well be paper - stored in closed
systems in unstructured formats that we can’t subsequently analyse or do computations over.

The opportunity cost of throwing away this information is huge. The truly revolutionary technologies and techniques that the
digital age has provided us are fuelled by data. Those techniques work best when you can feed them with structured, high
quality, granular data. Yet even at many world-renowned institutions in the NHS, the data infrastructure underpinning clinical
activity is distinctly 20th century.

Access to high quality clinical data by default has a transformative potential for the NHS. Improving patient care and optimising
our clinical services requires a real understanding of what we’re doing now - and that can only be obtained with data. Without that
data, we have no idea whether we’re even making things better.

And that’s before we even start with the promise of driving research and science by providing them with easily accessible, high
quality, computable clinical data.

## How do we help?

What we’ve found at Open Health Care, is that when you
[get the usability right](http://openhealthcare.org.uk/blog/2015/03/11/how-doctors-get-digital-services-they-love/)
for the end user - the person caring for a patient,
you can improve the efficiency and safety of patient care, while also capturing high granularity, research quality data as a part
of routine clinical care.

This is one of the reasons we created
[OPAL](https://github.com/openhealthcare/opal) - our Open Source platform for building clinical software applications. It pulls together
the results of years of usability testing with real clinicians, along with all of the hard thinking that we and others like us have
done about how to build robust digital tools for a health care environment.

Also built in to
[OPAL](opal.openhealthcare.org.uk/docs/v0.6.0/)
is the ability and the data modelling to collect the granularity of data required to enable us to provide
high quality data through extracts or Open APIs. We’ve explored how to balance the clinical user need of speed ease of use with
the system needs of quality data capture. Through a combination of pragmatic design, and frequent iteration, we’ve arrived at a
range of design patterns that give us the opportunity to design systems that work in the real world yet still enable subsequent
analysis.

For instance, we’ve built
[elCID](http://elcid.openhealthcare.org.uk/) - the first major application built using OPAL. It’s designed to help manage the care of
patients with infections, and it has been in use at
[University College Hospital London](https://www.uclh.nhs.uk/Pages/Home.aspx) for the last two and a half years in the
inpatient and outpatient services they run for patients with infections. It is used by clinicians day to day to manage the care of
patients, integrating with other hospital systems to pull key data from elsewhere in the trust, and it supports both clinical audit
and service development.

During that time it has improved the efficiency of clinical practice - saving time every single day by reducing work required in
the handover process for inpatient teams, and reducing significantly, the time required by Microbiology consultants to run their
liaison service to other parts of the trust - while providing robust documentation of that process for the first time.

It has supported the development of the
[OPAT service](http://openhealthcare.org.uk/blog/2015/02/05/elcid-opat-launch/)
- freeing up beds by allowing patients requiring IV antibiotics to be treated
as outpatients, saving the trust £1m per year. It also allows us to provide clinic managers realtime dashboards and management
reports about their activity, enabling them to make decisions with data that was previously unavailable to them.

In addition to this, data from the system has supported many clinical audits - making the process of collecting data to analyse
significantly faster, as well as
[one published academic paper](http://openhealthcare.org.uk/blog/2015/06/10/elcid-journal-of-infectioncontrol/),
two more in peer review, and six conference abstracts.

## How does it work?

Open Health Care provide digital tools to NHS institutions that help clinicians to deliver better care. We charge for support,
customisation and integration work, but we don’t charge for a license fee - all of our software is Open Source.

We provide either installations of existing products we have developed, or build bespoke solutions for the needs of the individual
organization we’re working with.

If you are interested in fining out how to get elCID at your organization, or have a project that involves clinical usability and
data then do [drop us a line](mailto:hello@openhealthcare.org.uk) - we’d love to hear from you.
