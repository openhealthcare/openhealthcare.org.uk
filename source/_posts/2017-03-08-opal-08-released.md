---
layout: post
title: "Opal 0.8 released"
date: 2017-03-08 14:00:29 +0000
comments: false
categories: opal
author: David Miller
author_link: thatdavidmiller
image: assets/images/posts/8.jpg
---
A few weeks ago now we released [Opal](http://opal.openhealthcare.org.uk) 0.8. It’s quite a large release, so we thought we’d
walk you through some of the highlights.

### Forms - now with added sugar

We’ve been spending lots of time working to make forms easier to work with. Sometimes it seems that 95% of designing services is making
forms that aren't frustrating and difficult to use
- and having good tools to quickly build and iterate the forms you’re working with can make that process much easier.

We made sure that some of the features from Django models, like choices and defaults now flow through seamlessly by default to our form
widgets, and that the client side Angular code will use these by default without you having to do anything. This was all possible before,
but required more typing. Nobody likes extra typing.

For instance, if we had the following model:

{% highlight python %}
    class TableClothPreference(EpisodeSubrecord):
        COLOUR_CHOICES = (
          ('P', 'Purple'),
          ('R', 'Red'),
        )
        favourite_colour = models.CharField(max_length=200,
                                            default='Purple',
                                            choices=COLOUR_CHOICES)
{% endhighlight %}

We would be able to render a dropdown widget for the field that used the default and restricted the choices by simply using the
following in our code:

{% highlight jinja %}
    { % select field="TableClothPreference.favourite_colour" % }
{% endhighlight %}

We’ve also spent time making sure that form validation is much easier to work with. By default we
now validate forms on submission - making sure that we respect max length of form fields for instance.

As well as the improvements to forms in Opal itself, we’ve also been working hard on the Opal
[Pathway library](https://github.com/openhealthcare/opal-pathway). This library makes it significantly easier to work with
complex forms - particularly ones that need to save data to many different models. Although Pathway is still considered alpha software,
we fully anticipate that we’ll be incorporating it into Opal itself as the recommended way to build forms in Opal applications later this year.

### Python 3 support

Responding to an issue raised on the mailing list, we’ve refactored Opal to work on Python 3. Thanks to the hard work and excellent tooling in the
Python community this was a relatively painless task, but hopefully it puts us in a good position to move towards Python 3 deployments moving forwards.

### Common patterns for customising Patient Lists

We’ve made it much easier to implement some of the common patterns we see when working with patient lists, by explicitly adding APIs.

You can now [customise the ordering](http://opal.openhealthcare.org.uk/docs/v0.8.0/guides/list_views/#customising-sort-order-of-episodes)
of patients on a list-by-list basis using the comparator_service attribute of PatientList classes.
A comparator service is an Angular service that returns a list of comparator functions that are used in order to determine how
we should compare and sort two episodes - for instance:

{% highlight javascript %}
    angular.module('opal.services')
        .factory('MyComparatorService', function(){
            "use strict";
            return [
                function(e){ return e.category_name },
                function(e){ return e.id }
            ]
        });
{% endhighlight %}

We also introduced an easy way for you to
[group lists into tabs](http://opal.openhealthcare.org.uk/docs/v0.8.0/guides/list_views/#grouping-related-patient-lists)
that display in the default template.

### Goodbye Angular-Strap

Until Opal 0.8 we had not one, but two UI libraries which wrapped Bootstrap components in Angular compatible code.
We’ve been uncomfortable about that for a while - it’s confusing to have to remember which widget comes from which
library! As of Opal 0.8 however we’ve picked a winner - [UI Bootstrap](http://angular-ui.github.io/bootstrap/versioned-docs/0.14.3/),
and we removed all references to Angular Strap completely, both in Opal and in all the applications and plugins we could find on
Github.

We're planning to update the UI Bootstrap library to a more recent version in the next couple of releases, but the re-naming of
their modal component could potentially make this transition slightly tricky, so we're waiting to make sure we can do so as
smoothly as possible.

### Finding out more

If you’d like to find out more about Opal, then you might like to try the
[documentation](http://opal.openhealthcare.org.uk/docs/) or the
[mailing list](https://groups.google.com/forum/?ohc-dev#!forum/ohc-opal).
There are more details about some of the other smaller features and bugfixes in 0.8 in the
[release notes](https://github.com/openhealthcare/opal/releases/tag/0.8.0),
and you
can also read about how to [upgrade from 0.7.x](http://opal.openhealthcare.org.uk/docs/v0.8.0/reference/upgrading/#071-080)
in the documentation.

If you have a project that you think might be suited to Opal, please do [get in touch](mailto:hello@openhealthcare.org.uk) - we’d love to hear from you.

<small>
Photo credits: [Jay Springett](https://www.flickr.com/photos/thejaymo/)
</small>
