---
selector: galerie
header: galerie
title: Ein paar <span>Eindrücke</span> aus unserem Laden
layout: default
order: 3
---

<div class="gallery-slider swiper h-25">
      <div class="swiper-wrapper align-items-center">
        {% for file in site.static_files %}
            {% if file.path contains '/assets/img/gallery' %}
                <div class="swiper-slide"><a class="glightbox" data-gallery="images-gallery" href="{{ site.baseurl }}{{ file.path }}"><img src="{{ site.baseurl }}{{ file.path }}" class="img-fluid" alt=""></a></div>
            {% endif %}
        {% endfor %}
      </div>
      <div class="swiper-pagination"></div>
</div>


