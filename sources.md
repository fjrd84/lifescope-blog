---
layout: page
title: "Data sources"
permalink: /sources/
---

Our application and the returned datasets are based on different health information sources. Currently, the Lifescope’s algorithm receives and analyzes the data from a live source like **Twitter**, and open-source medical databases such as **PubMed** or **ClinicalTrials** (we expect to add more in the future, such as news, non-specialized and specialized feeds).

Lifescope is programmed with a Twitter stream listener receiving a constant input of health data, as you can see in our application timeline.

<p align="center">
<img align="center" width="512" height="407" src="/assets/img/twitterlifescope.png">
</p>

&nbsp; 
&nbsp; 

In addition, our platform connects to [PubMed](https://www.ncbi.nlm.nih.gov/pubmed/) and [Clinical Trials](https://www.clinicaltrials.gov)' websites, as you can see in the following screenshots.

<p align="center">
<img align="center" width="520" height="325" src="/assets/img/pubmed.png">
</p>


&nbsp; 
&nbsp; 

We periodically receive **RSS feeds** from these websites with up-to-date **medical articles' metadata**, which provide us with very valuable medical research headlines and hyperlinks.

&nbsp; 

Sources' reliability
--------------------
As very different types of information are involved, both from Twitter and specialized databases, we must explore each source’s reliability, as this table shows.

| Source name | Source type | Reliability |
|:--------------------------|:------------------|:---------------|
| PubMed | Medical database | Highest |
| Clinical Trials | Medical database | Highest |
| Institution | Twitter | Very reliable |
| Academia | Twitter | Very reliable |
| Publishing source | Twitter | Very reliable |
| Doctor | Twitter | Very reliable |
| Professional | Twitter | Less reliable |
| Medical business | Twitter | Less reliable |
| Interested in healthcare | Twitter | Less reliable |
| News source | Twitter | Less reliable |
| Healthcare initiative | Twitter | Less reliable |
| Association | Twitter | Less reliable |
| Generic | Twitter | Less reliable |

We made a simple but effective reliability scale to categorize the sources being used. As you can see, medical databases are at the top of the scale, whereas a social network like Twitter holds a lower position. **We manually evaluated the user profiles' reliability on the 1023 test messages**, that were used in [the algorithm's confidence assessment](/confidence/).

&nbsp; 

Twitter's user profile categories
---------------------------------
As for Twitter, our algorithm was trained to return different reliability levels within a community of users providing healthcare information. For this reason, a key component of Lifescope is the **Twitter user profile analyzer**. It captures the most health-related profiles, and then assigns a category to each profile.

By using this system of categories, we expect to have lesser chances of receiving inputs from non-health (and non-wanted) related users. And yet, we can continue making a distinction among the incoming health-related users, as **the algorithm distinguishes different profiles**.

The following is a list of the 11 user profiles categorized by the algorithm, together with a definition and an example for each one (all these profiles are publicly available in Twitter).

&nbsp; 

+   **Institution**: Any kind of healthcare formal organization.

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/AADskin/status/953766892908498945"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Academia**: A health science researcher or lecturer

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/Schoffmonster/status/942790405170651137"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Doctor**: A self-described physician

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/headachedoc/status/950133426379685889"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Publishing source**: A medical serious publication

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/AmJPsychiatry/status/950780530173280256"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Professional**: A self-described expert in some health domain

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/TraeHook/status/964892231042846721"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Med Business**: A source related to medical products or companies

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/kiranshaw/status/982262451855962113"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Interested in healthcare**: Someone who expresses an interest in healthcare

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/eng_louise/status/960098816505589765"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **News source**: Any kind of medical news source.

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/THEMMEXCHANGE/status/977916534059184128"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Healthcare initiative**: A source related to a healthcare project or action plan

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/nclexpharm/status/920107188726706176"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Association**: Any kind of organization related to healthcare

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/NevadaBaseball/status/979504129633480705"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

&nbsp; 

+   **Generic**: Any other health-related sources

<blockquote class="twitter-tweet" data-lang="en">
<a href="https://twitter.com/VeganHealthDiet/status/983422333800116224"></a></blockquote>
<script async="" src="//platform.twitter.com/widgets.js" charset="utf-8"></script>