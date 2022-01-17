---
layout: default 
permalink: /categories/list/index.html 
title: Categories 
--- 
<!-- categories 1/2 -->
<div id="archives">
 {% for category in site.categories %} 

 <div class="archive-group">
 {% capture category_name %}{{ category | first }}{% endcapture %} 

<div id="#{{ category_name | slugize }}"></div> 

<p></p>

 <h3 class="category-head">{{ category_name }}</h3>
 <a name="{{ category_name | slugize }}"></a>

<!-- /categories 1/2 -->



<!-- categories 2/2 -->
 </div>

 {% endfor %}
 </div>
<!-- /categories 2/2 -->
