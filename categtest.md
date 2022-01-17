---
layout: default 
---


<hr>
<!-- categories -->
<div id="archives">
 {% for category in site.categories %} 
 <div class="archive-group">
 {% capture category_name %}{{ category | first }}{% endcapture %} 
<p></p>
 <h2 class="category-head">
  <a href="#{{ category_name | slugize }}" name="{{ category_name | slugize }}">{{ category_name | slugize }}</a>
 </h2>
 </div>
 {% endfor %}
 </div>
<!-- /categories -->
<HR>







