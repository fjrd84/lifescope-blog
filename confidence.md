---
layout: page
title: ""
permalink: /confidence/
---

Algorithm's confidence
----------------------
Click on the following preview for a detailed report on the algorithm's confidence level.

<a href="https://datastudio.google.com/embed/reporting/17i3EjWTInDBFbFK1ruNQyvw-ijbxFXk1/page/9zcN" target="blank">
![Alt text](/assets/img/confidence.png)
</a>

&nbsp;  
&nbsp; 

How do we evaluate it?
----------------------

We have manually tested **a sample of solutions and diseases** retrieved by the algorithm. A retrieved solution or disease is tested *True* or *False* **depending on how good or bad the algorithm performs in understanding natural language**. 

For example, Lifescope retrieves *botox* as solution, and *bruxism* as disease, in the following Twitter message:

> ![Alt text](/assets/img/Twitter-logo.png) Thank you for helping me spread the word about botox as a treatment for bruxism

&nbsp; &nbsp; ![Alt text](/assets/img/greendot.png) bottox (1) &nbsp; ![Alt text](/assets/img/greendot.png) bruxism (1)

&nbsp; 
&nbsp; 

Both retrieved items are **True** (both were properly understood as a treatment and a condition), hence we assign 1 to both the solution and the disease. If **False**, we assign 0, as in the first match of the following message:

> ![Alt text](/assets/img/Twitter-logo.png) Purkinje neuron degeneration on cerebellar ataxia

&nbsp; &nbsp; ![Alt text](/assets/img/reddot.png) purkinje neuron degeneration (0) &nbsp; ![Alt text](/assets/img/greendot.png) cerebellar ataxia (1)

&nbsp; 
&nbsp; 

And 0.5 to **poorly informative cases** as the following, where *screening* is OK, but the appropriate match would have been *screening of FOXD3*.

> ![Alt text](/assets/img/Twitter-logo.png) Screening of FOXD3 targets in lung cancer

&nbsp; &nbsp; ![Alt text](/assets/img/amberdot.jpeg) screening (0.5) &nbsp; ![Alt text](/assets/img/greendot.png) lung cancer (1)

&nbsp; 
&nbsp; 

Finally, note that **we are not evaluating the retrieved content, that is, if the solution is clinically good or bad, or even true or false**. For this reason, if the input text were *a purple lemon to prevent cancer*, we would assign 1 to *purple lemon* as a solution.

However, as the Lifescope's algorithm receives inputs only from healthcare-related users (see the [Sources](/sources/) section), we don't expect many purple lemon matches as a cancer therapy!