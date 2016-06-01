---
layout: post
title: "OPAL 0.5 released"
date: 2015-11-13 16:00:55 +0000
comments: true
categories:
        - opal
author: David Miller
author_link: thatdavidmiller
#image: assets/images/posts/london.bridge.jpg
---
We're happy to announce that we've just released a new version of [OPAL](http://opal.openhealthcare.org.uk/docs/) -
our framework for building clinical facing digital services.

So - what's new in this release?

## Search

We've completely re-designed our search pages to help clinicians find
the patients they're interested in more easily. We also default to
having a search box in the navigation of every page.

![](https://raw.githubusercontent.com/openhealthcare/openhealthcare.org.uk/master/source/assets/images/posts/search.results.png)

In addition, we've been working hard to make search backends pluggable,
so that in the future you'll be able to drop in alternative backends of
your choice as your application scales.

## Patient List view

We spent a lot of time over the past few months collating feedback from users and
doing research to understand how we could improve the core Patient List
views. As a response to that we've updated the list interface - making it clearer
which patient is currently active, and removing some of the features that weren't
actually helping our users to care for patients.

![](https://raw.githubusercontent.com/openhealthcare/openhealthcare.org.uk/master/source/assets/images/posts/list.view.png)

## Subrecord metadata

We added four new utility fields to
[Patient and Episode subrecords](http://opal.openhealthcare.org.uk/docs/guides/datamodel/)
 - created_by, updated_by, created, updated. This gives developers easier
programatic access to high level audit trail information, without having
to navigate the [low level Django Reversion
API](https://github.com/etianen/django-reversion/blob/master/docs/api.rst)
- which is still there for when you need more detailed audit trail
information.

## Select2 and List fields

This release introduces
[Select2](https://github.com/angular-ui/ui-select) to OPAL - which
provides us some nicer widgets - particularly for fields associated with
[lookuplists](http://opal.openhealthcare.org.uk/docs/guides/lookup_lists/),
and has also enabled the development of list types as
Subrecord fields. For example this means that your travel can be to a
list of countries when you take a backpacking trip through Southeast
Asia!

## What's Next?

Just because this release is out, we're not resting on our laurels - in
fact we're already gearing up for the next releases. We're planning to
look at the information architecture of Episode detail views, including
a new Notes view that's currently being tested by some users of the
[elCID](http://elcid.openhealthcare.org.uk) project.

We also plan to refactor some of the core data models back into OPAL to provide
them there by default rather than implemented over and over again in
individual applications.

As ever, because OPAL is an Open Governance [Open Source](http://github.com/openhealthcare/opal) project, you can
follow our progress over on
[our public Waffle board](https://waffle.io/openhealthcare/opal-ideas) where we'll be
organising our work.

## More about OPAL

If you want to find out more about OPAL or how Open Health Care can help
you to run high quality digital services for doctors in your institution
then do get in touch!
