---
layout: post
title: "What is the most cited retracted paper?"
date: 2015-04-16 15:11:56 +0000
comments: true
categories:
author: Carl
author_link: drcjar
image: assets/images/posts/retraction.jpg 
---

At Open Health Care we believe in
[Evidence Based Medicine](http://en.wikipedia.org/wiki/Evidence-based_medicine).

Which is why we create digital health [services that support research](https://github.com/openhealthcare/opal-research).

Unfortunately the current infrastructure supporting evidence based medicine has some shortcomings. One of these is that
when a research paper is retracted because, for example, [the author](http://en.wikipedia.org/wiki/Hwang_Woo-suk)
[made up the results](http://en.wikipedia.org/wiki/Scientific_misconduct), there is little or no means 
to propogate this update in the wider medical literature.

Supposing, as a doctor, I look to a systematic review on the management of heart attacks to inform how I treat my patient, 
I sadly have no assurance that the systematic review does not rely on research papers that have been retracted. This is suboptimal.

Open access, post-publication peer review, and better version control would be three useful features that a modern scientific 
publishing model optimized to enable good science should support.

In the meantime, inspired by a lunchtime conversation with our friend and director Ben Goldacre (it was all his idea),
we pondered the question:

<blockquote class="custom-quote"><p><i class="fa fa-question fa-3x"></i>
What is the most cited retracted paper?
</p></blockquote>

It turns out [PubMed](http://www.pubmed.gov) already has a nice API that can return a 
[list](http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&retmode=json&retmax=10000&term=%22retracted%20publication%22) 
of PubMed ids for papers that have been retracted. Next we needed a means of knowing how many times each retracted paper was cited. 
There are a few ways of doing this but we went with using google scholar after Alf Eaton told us about it on 
[twitter](https://twitter.com/invisiblecomma/status/582904870644113408). It's possible to search google scholar for the articles 
citing a particular pubmed id, here's an [example](https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/19336536).

Finally, we used wget to download all of the google scholar search results.  This infamous 
[paper](http://www.thelancet.com/journals/lancet/article/PIIS0140-6736%2897%2911096-0/abstract) 'Ileal-lymphoid-nodular hyperplasia, 
non-specific colitis, and pervasive developmental disorder in children.' was the winner with 
2070 [citations](https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/9500320)!

Here's the top ten:

<table class="table table-striped">
<tbody><tr><td>Citations</td>
<td colspan="2">Title</td>
<td>Author</td>
<td>Journal</td>
<td>Pubdate</td>
</tr>
<tr><td>2070</td>
<td colspan="2"><a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/9500320">
Ileal-lymphoid-nodular hyperplasia, non-specific colitis, and pervasive developmental disorder in children.
</a>
</td>
<td>Wakefield AJ</td>
<td>Lancet</td>
<td>28/02/1998</td>
</tr>
<tr><td>2050</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/15604363">
Visfatin: a protein secreted by visceral fat that mimics the effects of insulin.
</a>
</td>
<td>Fukuhara A</td>
<td>Science (New York, N.Y.)</td>
<td>21/01/2005</td>
</tr>
<tr><td>1550</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/11675329">
Purification and ex vivo expansion of postnatal human marrow mesodermal progenitor cells.
</a>
</td>
<td>Reyes M</td>
<td>Blood</td>
<td>01/11/2001</td>
</tr>
<tr><td>1250</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/12531578">
Combination treatment of angiotensin-II receptor blocker and angiotensin-converting-enzyme inhibitor in non-diabetic renal disease (COOPERATE): a randomised controlled trial.
</a>
</td>
<td>Nakao N</td>
<td>Lancet</td>
<td>11/01/2003</td>
</tr>
<tr><td>1040</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/15833829">
Spontaneous human adult stem cell transformation.
</a>
</td>
<td>Rubio D</td>
<td>Cancer research</td>
<td>15/04/2005</td>
</tr>
<tr><td>825</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/10700237">
Regression of human metastatic renal cell carcinoma after vaccination with tumor cell-dendritic cell hybrids.
</a>
</td>
<td>Kugler A</td>
<td>Nature medicine</td>
<td>01/03/2000</td>
</tr>
<tr><td>805</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/14963337">
Evidence of a pluripotent human embryonic stem cell line derived from a cloned blastocyst.
</a>
</td>
<td>Hwang WS</td>
<td>Science (New York, N.Y.)</td>
<td>12/03/2004</td>
</tr>
<tr><td>755</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/12176951">
Multiple atherosclerotic plaque rupture in acute coronary syndrome: a three-vessel intravascular ultrasound study.
</a>
</td>
<td>Rioufol G</td>
<td>Circulation</td>
<td>13/08/2002</td>
</tr>
<tr><td>732</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/11546864">
Structure of MsbA from E. coli: a homolog of the multidrug resistance ATP binding cassette (ABC) transporters.
<a/>
</td>
<td>Chang G</td>
<td>Science (New York, N.Y.)</td>
<td>07/09/2001</td>
</tr>
<tr><td>616</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/8633243">
Synergistic activation of estrogen receptor with combinations of environmental chemicals.
</a>
</td>
<td>Arnold SF</td>
<td>Science (New York, N.Y.)</td>
<td>07/06/1996</td>
</tr>
<tr><td>607</td>
<td colspan="2">
<a href="https://scholar.google.com/scholar?cites=http://www.ncbi.nlm.nih.gov/pubmed/12351674">
Contribution of human alpha-defensin 1, 2, and 3 to the anti-HIV-1 activity of CD8 antiviral factor.
</a>
</td>
<td>Zhang L</td>
<td>Science (New York, N.Y.)</td>
<td>01/11/2002</td>
</tr>
</tbody></table>

You can reproduce our results or view our workings [over on Github](https://github.com/davidmiller/retractions).

There are of course many reasons other than the author making up the results for a paper to be retracted. There are also many circumstances 
in which citing a retracted paper is legitimate. For a more nuanced discussion of retractions there's a nice [Comprehensive Survey of 
Retracted Articles from the Scholarly Literature](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0044118) in PLOS and the 
excellent [Retraction Watch](http://retractionwatch.com/) covers the details of individual retractions as they happen.

Anyway, it was fun to examine retractions. We'd love to explore this further so if we can be of service to you do get in touch.

Perhaps a project for [NHS Hack Day](http://www.nhshackday.com)?
