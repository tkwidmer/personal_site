---
layout: portfolio
title: Portfolio
permalink: '/galleries/'
redirect_from:
  - '/portfolio/'

---

<h1> Portfolio </h1>

<div class="row">
  <div class="col-md-10">
    <p> I've been making photographs for about twelve years. I first picked up a manual metal-cased Canon SLR, but these days I shoot a Canon 7D and a Fujifilm X100-T. I enjoy shooting events, environmental portraits, and landscapes / architecture. If you are in need of a photographer, please <a href="/contact/"> contact me</a>.
    </p>
  </div>
</div>

<ul class="gallery index-gallery">
  {% assign sorted_galleries = site.galleries | sort:"index" %}

  {% for gallery in sorted_galleries %}
    {% if gallery.excluded == true %}
      {% continue %}
    {% endif %}

    <li class="thumbnail-wrap">
      <h5 class="text-center">
        {{gallery.title}}
      </h5>
      <a class="thumbnail" href="{{gallery.url}}">
        <div class="gallery-img"
          style="background-image: url('{{gallery.featured_image_path}}')">
        </div>

      </a>
    </li>
  {% endfor %}
</ul>
