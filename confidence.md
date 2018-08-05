---
layout: page
title: "Algorithm's confidence"
permalink: /confidence/
---
  
[![Alt text](/assets/img/confidence.png)](https://datastudio.google.com/embed/reporting/17i3EjWTInDBFbFK1ruNQyvw-ijbxFXk1/page/9zcN)
*Click on this preview for a detailed report on the algorithm's confidence level*
&nbsp;  
&nbsp; 

Algorithm's performance: How do we evaluate it?
-----------------------------------------------

We have manually tested **a sample of solutions and diseases** retrieved by the algorithm. A retrieved solution or disease is tested *True* or *False* **depending on how good or bad the algorithm performs in understanding natural language**. 

For example, Lifescope retrieves *botox* as solution, and *bruxism* as disease, in the following Twitter message:

> ![Alt text](/assets/img/twitterchico.png) Thank you for helping me spread the word about botox as a treatment for bruxism

{% highlight javascript%}
'botox' = 1.0
'bruxism' = 1.0
{% endhighlight %}

&nbsp; 
&nbsp; 

Both retrieved items are **True** (both were properly understood as a treatment and a condition), hence we assign **1.0** to both the solution and the disease. If **False**, we assign **0**, as in

> ![Alt text](/assets/img/twitterchico.png) Purkinje neuron degeneration on cerebellar ataxia

{% highlight javascript%}
'purkinje neuron degeneration' = 0
'cerebellar ataxia' = 1.0
{% endhighlight %}

&nbsp; 
&nbsp; 

And **0.5 to poorly informative cases**, as the following, where *screening for lung cancer* is OK, but the appropriate text match is *screening of FOXD3*.

> ![Alt text](/assets/img/twitterchico.png) Screening of FOXD3 targets in lung cancer

{% highlight javascript%}
'screening for lung cancer' = 0.5
'lung cancer' = 1
{% endhighlight %}

&nbsp; 
&nbsp; 

Finally, note that **we are not evaluating the retrieved content, that is, if the solution is clinically good or bad, or even true or false**. For this reason, if the input text were a purple lemon to prevent cancer, we would assign 1.0 to a purple lemon as a solution.

However, as the Lifescope's algorithm receives inputs only from healthcare-related users (see the [link]Sources section), we don't expect many purple lemon matches as a cancer therapy!