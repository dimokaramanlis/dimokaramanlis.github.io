---
layout: default
---

<style>
  .justified-text p {
    text-align: justify;
  }
</style>

<div class="justified-text" markdown="1">


Welcome! I'm Dimos (Δήμος), a neuroscientist and postdoctoral researcher at the University of Geneva. My research is driven by fundamental questions about neural computation: How do neuronal populations integrate inputs across diverse timescales and brain areas? And how does this integration adapt during learning? I enjoy designing novel experimental and analytical approaches to tackle these frontier problems, combining high-throughput behavior, large-scale electrophysiology *in vivo*, brain-wide activity mapping, and statistical modeling.

<!---
[/I focus on understanding the retinal encoding of natural scenes. I work at the interface of computational neuroscience and large-scale electrophysiology. /]
# We showed that such nonlinear operations drive correlated and redundant responses of retinal ganglion cells during gaze shifts, and illustrated that such responses may require the reevaluation of the efficient coding theory. 
-->

In the [El-Boustani lab](http://elboustani-lab.org/), I'm currently studying how frontal cortical areas represent information about others during social decision-making. My doctoral work with [Tim Gollisch](https://www.retina.uni-goettingen.de/) focused on how nonlinear processing shapes the encoding of natural scenes in the mammalian retina. I have previously studied Neuroscience at the [IMPRS Göttingen](https://www.gpneuro.uni-goettingen.de/) and Medicine at the [Aristotle University of Thessaloniki](https://www.auth.gr/en/). 

You can find my CV [here](./cv_word.pdf).

</div>
---


<div class="news">
<h2><a href="./news">News</a></h2>
{% if site.news  -%} 
<div class="table-responsive">
  <table class="table table-sm table-borderless">
  {%- assign news = site.news | reverse -%} 
  {% for item in news limit: site.news_limit %} 
	<tr>
	  <th scope="row">{{ item.date | date: "%Y/%m/%d" }}</th>
	  <td>
		{% if item.inline -%} 
		  {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
		{%- else -%} 
		  <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
		{%- endif %} 
	  </td>
	</tr>
  {%- endfor %} 
  </table>
</div>
{%- else -%} 
<p>No news so far...</p>
{%- endif %} 
</div>
