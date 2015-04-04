---
layout: post
title: "Which retracted paper has the most citations?"
date: 2015-03-31 15:11:56 +0000
comments: true
categories:
author: Carl
author link: drcjar
image: assets/images/posts/retractionwatch.jpg 
---

At Open Health Care we believe in
[Evidence Based Medicine](http://en.wikipedia.org/wiki/Evidence-based_medicine). 

Which is why we create digital health services support research.

Unfortunately the current infrastructure supporting evidence based medicine has some shortcomings. One of these is that
when a research paper is retracted because, for example, the author made up the results, there is little or no means to propogate this update in the wider medical literature.

Supposing, as a doctor, I look to a systematic review on the management of heart attacks to inform how I treat my patient, I sadly have no assurance that the systematic review does not rely on research papers that have been retracted. This is suboptimal.   

Our friend and director Ben Goldacre has been planning a retractions database to help to address this problem for a while. This afternoon we decided to explore the problem by making up the question which retracted paper has the most citations?

It turns out [pubmed](http://www.pubmed.gov) has a nice API that can return a list of pubmed ids for papers that have been retracted. [Here](http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&retmode=json&retmax=10000&term=%22retracted%20publication%22) is the list. Next we needed a means of knowing how many times each retracted paper was cited. There are a few ways of doing this but we went with using google scholar after [Alf Eaton](https://twitter.com/invisiblecomma) put us right on twitter. It's possible to search google scholar for the articles citing a particular pubmed id in the following way 
[https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/25451150]


If we could get a feed of, say every paper cited in a cochane review, we could then build a service to detect retractions cited in [cohrane reviews](http://www.cochranelibrary.com/) and respond to them appropriately. 

In fact we've already built most of this and it would be nice to improve evidence based medicine infrastructure in this way :-)    
