---
layout: page
title: We Exist
permalink: '/photography/we-exist/'
---
<div class="row">
  <div class="col-sm-12">
    <img src="https://40.media.tumblr.com/919c055178e307393ddd684d7ab5bc2b/tumblr_nladwaMUA31qz7dx8o1_1280.jpg" style="border-radius: 7px">
    <p class="headroom">
      Trans folk who were assigned male at birth are often made invisible and forgotten by the communities and spaces in which they exist every day. The leather and BDSM communities are no different. The contributions and mere presense of trans women are often ignored. <em> We Exist </em> is a photo essay that seeks to highlight the faces and stories of trans women who exist in leather and BDSM communities.
    </p>

    <p>
      If you would like to be a part of this project please email me at tkwidmer [at] gmail [dot] com. I am local to the San Francisco bay area.
    </p>

  </div>
</div>

<hr class="headroom">

<div class="row headroom">
  {% for profile in site.data.we_exist %}
    <div class="col-xs-12 col-sm-6 col-md-4">
      <img src="{{profile.image}}" style="border-radius: 7px">
      <div class="headroom">
        <h4>#{{ profile.number}} - {{ profile.name }} </h4>
        <p>
          {{ profile.summary }}
        </p>
      </div>
    </div>
  {% endfor %}
</div>
