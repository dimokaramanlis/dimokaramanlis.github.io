---
layout: default
---

My name is Dimos and I’m a doctoral student in the [Gollisch lab](https://www.retina.uni-goettingen.de/) at the University Medical Center Göttingen under the supervision of Tim Gollisch.

My research focuses on the retinal encoding of natural scenes. I work at the interface of computational neuroscience and large-scale electrophysiology.

I have previously studied Neuroscience at the [IMPRS Göttingen](https://www.gpneuro.uni-goettingen.de/) and Medicine at the [Aristotle University of Thessaloniki](https://www.auth.gr/en/). You can find my CV [here](./karamanlis_cv.pdf).


<div class="news">
<h3>News</h3>
{% if site.news  -%} 
<div class="table-responsive">
  <table class="table table-sm table-borderless">
  {%- assign news = site.news | reverse -%} 
  {% for item in news limit: site.news_limit %} 
	<tr>
	  <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
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

