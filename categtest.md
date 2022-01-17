---
layout: default
title: ise.pc-cdn.de - Quellennachweise 
---

<div id="home">
  <h1>verwendete Grafiken/Ressourcen</h1>
<p>Ein Teil der im {{ site.label }} verwendeten Bilder und sonstigen Ressourcen stammt von diversen Quellen / Bilderdiensten. <br />
Das Copyright dieser Bilder und sonstigen Ressourcen liegt bei den jeweiligen Urheber. <br />
Hier finden Sie Angaben zu den Quellen der verwendeten Bilder/Ressourcen. </p>

<p>Mit einem Klick auf das Bild erhalten Sie weitere Informationen und jeweils (sofern vorhanden) den Link zum Original der jeweiligen Quelle.</p>


<hr>


<!-- categories -->
<div id="archives">
 {% for category in site.categories %} 

 <div class="archive-group">
 {% capture category_name %}{{ category | first }}{% endcapture %} 

<div id="#{{ category_name | slugize }}"></div> 

<p></p>

 <h3 class="category-head">{{ category_name }}</h3>
 <a href="#{{ category_name | slugize }}" name="{{ category_name | slugize }}">{{ category_name | slugize }}</a>
 </div>

 {% endfor %}
 </div>
<!-- /categories -->



<ul class="posts">
  {% for post in site.posts %}

<article id="{{ post.id }}" class="{{ post.id }}{{ post.tags }} post type-post status-publish format-standard hentry">
	<header class="entry-header">
		<h1 class="entry-title"><a href="{{ post.url }}" rel="bookmark">{{ post.title }}</a></h1>
		<span class="entry-format-badge genericon genericon-standard"><span class="screen-reader-text">Standard</span></span>
	</header><!-- .entry-header -->
     <div class="entry-content">
	<blockquote>
	 <p style="text-align: center;">
          <a href="{{ post.url }}" rel="bookmark">
           <img src="/assets/img/bg/overlay-pattern.png" 
           style="background-image: url(/assets/img/post-thumbnails/{{post.thumbnail}}); background-repeat: no-repeat; background-position: center center;" 
           loading="lazy" class="alignnone wp-image-50 aligncenter"
           width="150" height="150" alt="{{ post.title }}"> {{ post.title }}</p>
          </a>
	 <p>&nbsp;</p>
	</blockquote>
     </div>
<!-- .entry-content -->
		<footer class="entry-meta">
		<ul class="clear">
	<li class="date-meta">
		<div class="genericon genericon-month"></div>
		<span class="screen-reader-text">date</span>
		<a href="{{ post.url }}" rel="bookmark" title="{{ post.date | date_to_string }}">{{ post.date | date_to_string }}</a>
	</li>
			</ul>
	</footer><!-- .entry-meta -->
	</article><!-- #post-## -->

    {% endfor %}
  </ul>



</div>
