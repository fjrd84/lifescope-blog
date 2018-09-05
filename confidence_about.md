---
layout: page
title: ""
permalink: /confidence_about/
---


How do we evaluate it?
----------------------

We have manually tested **a sample of solutions and diseases** retrieved by the algorithm. A retrieved solution or disease is tested *True* or *False* **depending on how good or bad the algorithm performs in understanding natural language**. 

For example, Lifescope retrieves *botox* as solution, and *bruxism* as disease, in the following Twitter message:

*Thank you for spreading the word about <span class="solution">botox</span> as a treatment for <span class="problem">bruxism</span>*  &nbsp; &nbsp; <span class="test">1 + 1</span>

&nbsp; 

Both retrieved items are **True** (both were properly understood as a treatment and a condition), hence we assign 1 to both the solution and the disease. If **False**, we assign 0, as in the first match of the following message:

*<span class="solution">Purkinje neuron degeneration</span> on <span class="problem">cerebellar ataxia</span>* &nbsp; &nbsp; <span class="test">0 + 1</span>

&nbsp; 

And 0.5 to **poorly informative cases** as the following, where *screening* is OK, but the appropriate match would have been *screening of FOXD3*.

*<span class="solution">Screening</span> of FOXD3 targets in <span class="problem">lung cancer</span>* &nbsp; &nbsp; <span class="test">0.5 + 1</span>

&nbsp; 

Finally, note that **we are not evaluating the retrieved content, that is, if the solution is clinically good or bad, or even true or false**. For this reason, if the input text were *a purple lemon to prevent cancer*, we would assign 1 to *purple lemon* as a solution.

However, as the Lifescope's algorithm receives inputs only from healthcare-related users (see the [Sources](/sources/) section), we don't expect many purple lemon matches as a cancer therapy!

||
|:--|
|[<span class="subsection"> < Confidence report</span>](/confidence/)|