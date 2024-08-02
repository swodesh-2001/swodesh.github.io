---
layout: page
title: Purpose-Passion
permalink: /passion
subtitle: My Purpose and Passion
nav: true
nav_order: 2
horizontal: false
---

## Sustainable Energy Production and Distribution

As an electrical engineer passionate about sustainable energy, my mission is to contribute to power electronics, renewable integration, and grid stability. With the increase in renewable penetration in grid, we must design a system capable of making it stable. This comes with creating better converters, better optimization and resilience techniques

<div class="image-container">
    <img src="/assets/img/Misc/sustainable.png" alt="Sustainable Image" class="responsive-image">
</div>

With the growing energy demands driven by training Large Language Models (LLMs), Electric Vehicles, More Computing need of a normal individual, the grid will reach its limit soon.So, to be prepared for the upcoming challenges, `I aim to collaborate and do research on AI algorithms for power electronics and power system for efficient renewable energy integration and maintaining grid stability`.  

## Contributing to Surgical Simulation for Low and Middle-Income Countries

My second life mission is to impact low and middle-income countries in health sector. `The disparity in healthcare resources between developed and developing nations is significant.` To address this, `my team and I are developing a low-cost laparoscopic simulator box` to provide affordable surgical training tools for doctors in these regions. 

By integrating computer vision (`Classical + Deeplearning`) algorithms and designing low cost simulator device capable of running these model, we believe it will create a massive impact.

Here are some of our initial accomplishments : 

<div class="slideshow-container">

  <div class="mySlides">
    <img src="/assets/img/Laapsi/Pic1.jpg" style="width:100%">
    <div class="text"> Hardware prototype for the Automated Progress Tracking Simulator and our Silicon model</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/Laapsi/Pic2.jpg" style="width:100%">
    <div class="text">Software Prototype</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/Laapsi/Pic3.jpg" style="width:100%">
    <div class="text">Me and Automated Progress Tracking Simulator</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/Laapsi/Pic4.jpg" style="width:100%">
    <div class="text">Showcasing our prototype in Manipal Hospital, Pokhara</div>
  </div>

  <div class="mySlides">
    <img src="./assets/img/Laapsi/Pic5.jpg" style="width:100%">
    <div class="text">Validation from Dr. Surgeon Jeremy</div>
  </div>

  <div class="mySlides">
    <img src="./assets/img/Laapsi/Pic6.jpg" style="width:100%">
    <div class="text">Our Team</div>
  </div>

  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>

</div>

<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span> 
  <span class="dot" onclick="currentSlide(2)"></span> 
  <span class="dot" onclick="currentSlide(3)"></span> 
  <span class="dot" onclick="currentSlide(4)"></span> 
  <span class="dot" onclick="currentSlide(5)"></span> 
</div>

---

<style>
.slideshow-container {
  position: relative;
  margin: auto;
  max-width: 600px;
}

.mySlides {
  display: none;
}


.mySlides img {
  width: 100%;
  height: 300px; /* Set a fixed height for all images */
  object-fit: contain; /* Ensures the images scale proportionally and cover the fixed height */
}


.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  user-select: none;
}

.next {
  right: 0;
}

.text {
  color: #000; /* Set to black for better visibility */
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
  background-color: rgba(255, 255, 255, 0.7); /* Semi-transparent white background */
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.dot.active {
  background-color: #717171;
}

.image-container {
    width: 50%; 
    display: flex;
    justify-content: center;
    align-items: center;
}

.responsive-image {
    max-width: 100%;
    height: auto;
    display: block;
}

</style>

<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  slides[slideIndex-1].style.display = "block";
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  dots[slideIndex-1].className += " active";
}
</script>
