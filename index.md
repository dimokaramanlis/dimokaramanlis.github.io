---
layout: default
---

My name is Dimos and I’m a postdoctoral fellow in the [El-Boustani lab](http://elboustani-lab.org/) at the University of Geneva. My research focuses on social decision-making and how frontal cortical areas represent information about others. To tackle questions in these areas, I combine high-throughput behavioral experiments, large-scale electrophysiology and imaging *in vivo*, and statistical modeling.

<!---
[/I focus on understanding the retinal encoding of natural scenes. I work at the interface of computational neuroscience and large-scale electrophysiology. /]
-->

My doctoral work with [Tim Gollisch](https://www.retina.uni-goettingen.de/) focused on how nonlinear processing shapes the retinal encoding of natural scenes. I have previously studied Neuroscience at the [IMPRS Göttingen](https://www.gpneuro.uni-goettingen.de/) and Medicine at the [Aristotle University of Thessaloniki](https://www.auth.gr/en/). 

You can find my CV [here](./cv_word.pdf).

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
