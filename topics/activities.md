---
layout: default
---

<section class="section bg-secondary">
  <div class="container">
    <div class="row">
      <div class="col-lg-12">
        <h2>{{ page.title }}Activities</h2>
      </div>
    </div>
  </div>
</section>
<!-- /page-title -->

<section>
  <div class="container">
	<br/><br/>
	<a class="text-dark" href="../activities-list">List view</a>
  </div>
</section>

<!-- category post -->
<section>
  <div class="container">
    <div class="row">
      <div class="col-lg-8">
        <div class="row masonry-container pt-5">
          {% assign activities_posts = site.posts | where_exp: "post", " post.categories contains 'Activities' " %}
          {% for post in activities_posts %}

          <div class="col-sm-6 mb-5">
            <article class="text-center">
              <img class="img-fluid mb-4" src="{{post.image | relative_url }}" alt="{{post.title}}">
              {% for category in post.categories %}
              <a class="d-block mb-3 text-dark text-uppercase" href="{{ 'topics/' | relative_url }}{{ category | slugify }}">{{ category }}</a>
              {% endfor %}
              <h4 class="title-border"><a class="text-dark" href="{{ post.url | relative_url }}">{{post.title}}</a></h4>
              <p>{{ post.content | strip_html | truncatewords: 35 }}</p>
              <a href="{{ post.url | relative_url }}" class="btn btn-transparent">read more</a>
            </article>
          </div>
          {% endfor %}
        </div>
      </div>
      <!-- /blog post -->
      {% include sidebar.html %}
      </div>
    </div>

</section>
<!-- /category post -->