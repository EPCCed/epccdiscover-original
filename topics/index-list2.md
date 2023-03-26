---
layout: section
title: Leaflets
banner: web_banners_10.jpg
tags: [Chemistry and Materials, Earth Sciences and Environment, Engineering and Energy,  Mathematics and Computer Science]
---

  



<!-- Now display all the posts, in date code order, newest first -->

{% assign leaflet_posts = site.posts | where_exp: "post", " post.categories contains 'Leaflets' " %}
     {% for post in leaflet_posts %}



<div class="casestudy">

	<div class="csimage">
		<a href="{{ post.url | relative_url }}"><img
			src="{{site.base_url}}/{{ post.image }}" alt="{{ post.title }}" title="{{ post.title }}" style="width: 200px;" /></a>
	</div>

	<div class="cstext">


			<a href="{{ post.url | relative_url }}">{{ post.title }}</a>
	





		<p>
          {{ post.content | strip_html }}
		 
           Read more...</a>
		</p>

	</div>
</div>






{% endfor %}







