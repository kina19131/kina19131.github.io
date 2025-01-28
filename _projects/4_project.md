---
layout: page
title: Bike
description: Biking around cities
img:
importance: 1
category: hobbies
---

I love exploring the city on a bike. I bike around 350 days out of 365 days. 
Yes, sometimes I do go out when there's snow outside (cause am in Canada). 

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bike1.JPG" title="Welcome to Toronto" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bike2.jpg" title="Bike in Rain" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bike3.jpeg" title="Bike in Vancouver" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Biking here and there and everywhere
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/bike4.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/bike5.JPG" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Oh yes I had to make sure no one was near when I took these shots
</div>

It is so refreshing to hit the road and feel the wind. 
