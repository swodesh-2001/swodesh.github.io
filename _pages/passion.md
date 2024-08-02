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

As an electrical engineer passionate about sustainable energy, my mission is to contribute to power electronics, renewable integration, and grid stability. The future demands a sustainable approach to energy production and distribution.

I am dedicated to promoting renewable energy sources and integrating them into existing power grids. With the growing energy demands driven by Large Language Models (LLMs), ensuring our energy infrastructure can meet these needs sustainably is crucial. My focus is on developing innovative solutions for efficient renewable energy integration and maintaining grid stability amid the rise of electric vehicles and the decline of fossil fuels.

## Contributing to Low and Middle-Income Countries

My second mission is to impact low and middle-income countries. The disparity in healthcare resources between developed and developing nations is significant. To address this, my team and I are developing a low-cost laparoscopic simulator box to provide affordable surgical training tools for doctors in these regions.

## Photo Gallery

<div class="slideshow-container">

  <div class="mySlides">
    <img src="/assets/img/certificates/Deep_Learning_Specialization/Course3.png" style="width:100%">
    <div class="text">Description of Image 1</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/certificates/Deep_Learning_Specialization/Course2.png" style="width:100%">
    <div class="text">Description of Image 2</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/certificates/Deep_Learning_Specialization/Course3.png" style="width:100%">
    <div class="text">Description of Image 3</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/certificates/Deep_Learning_Specialization/Course2.png" style="width:100%">
    <div class="text">Description of Image 4</div>
  </div>

  <div class="mySlides">
    <img src="/assets/img/certificates/Deep_Learning_Specialization/Course3.png" style="width:100%">
    <div class="text">Description of Image 5</div>
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

By pursuing these missions, I aim to create a sustainable and equitable future, ensuring the energy sector and healthcare systems are ready for tomorrow's challenges.

<style>
.slideshow-container {
  position: relative;
  margin: auto;
  max-width: 600px;
}

.mySlides {
  display: none;
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
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
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
