---
layout: page
title: We Exist
permalink: '/photography.html'
---

<h1> Photography </h1>

<p> I've been making photographs for about twelve years. I first picked up a manual metal-cased Canon SLR, but these days I shoot a Canon 7D. I enjoy shooting events, enviormental portraits, and landscapes / architecture. If you are in need of a photographer, please contact me at {{ site.email }}
</p>

<hr class="headroom">

<div class="row">
  <div class="col-sm-2">
    <ul class="nav nav-pills nav-stacked vspace2 gallery-nav" role="tablist">
      {% for gallery in site.data.galleries %}

        {% if forloop.first %}
          {% assign activeClass = 'active' %}
        {% else %}
          {% assign activeClass = '' %}
        {% endif %}

        <li role="presentation" class="{{ activeClass }}">
          <a data-target="#{{ gallery.id }}" aria-controls="{{ gallery.id }}" role="tab" data-toggle="tab">
            {{ gallery.display_name }}
          </a>
        </li>
      {% endfor %}
    </ul>
  </div>
  <div class="col-sm-10">
    <div class="tab-content vspace2">

      {% for gallery in site.data.galleries %}
        {% if forloop.first %}
          {% assign activeClass = 'active' %}
        {% else %}
          {% assign activeClass = '' %}
        {% endif %}

        <div role="tabpanel" class="tab-pane {{ activeClass }}" id="{{ gallery.id }}">
            {% for image in gallery.images %}
              <div class="col-xs-6 col-md-4">
                <a class='thumbnail' href="{{ image.path }}" data-lightbox="{{ gallery.id }}" data-title="{{ image.title }}">
                  <div class="gallery-img" style="background-image: url('{{ image.path }}');">
                  </div>
                </a>
              </div>
            {% endfor %}
        </div>
      {% endfor %}
    </div>
  </div>
</div>


<!-- <div class="row headroom">
  {% for profile in site.data.portfolio %}
    <div class="col-xs-6 col-md-4">
      <a href="{{profile.image}}" data-lightbox="we-exist" data-title="{{ profile.name }}">
        <img src="{{profile.image}}" style="border-radius: 7px">
      </a>
    </div>
  {% endfor %}
</div>
 -->

<!--


<hr class="headroom">

<div class="row headroom">
  {% for profile in site.data.portfolio %}
    <div class="col-xs-6 col-md-4">
      <a href="{{profile.image}}" data-lightbox="we-exist" data-title="{{ profile.name }}">
        <img src="{{profile.image}}" style="border-radius: 7px">
      </a>
    </div>
  {% endfor %}
</div> -->