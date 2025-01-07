---
layout: page
title: Featured Highlights
permalink: /highlights
subtitle: Achievements, Projects, and Awards
nav: true
nav_order: 8
horizontal: false
---


Some Memorable Undergrad Memories

<div class="slider-container">
  <div class="slider">
    <div class="slide">
      <img src="/assets/img/highlights/6.jpeg" alt="Volunteering at IEEE RESSD Conference" onclick="enlargeImage(this)">
      <div class="text">Volunteering at IEEE RESSD Conference</div>
    </div>
    <div class="slide">
      <img src="/assets/img/highlights/2.png" alt="Lecturing juniors on Circuit and PCB design in Proteus." onclick="enlargeImage(this)">
      <div class="text">Lecturing juniors on Circuit and PCB design in Proteus.</div>
    </div>
    <div class="slide">
      <img src="/assets/img/highlights/3.png" alt="With Project Supervisor and Team on Final Thesis Submission Day." onclick="enlargeImage(this)">
      <div class="text">With Project Supervisor and Team on Final Thesis Submission Day.</div>
    </div>
    <div class="slide">
      <img src="/assets/img/highlights/4.jpeg" alt="Energy Hackathon Winning Moment" onclick="enlargeImage(this)">
      <div class="text">Energy Hackathon Winning Moment</div>
    </div>
    <div class="slide">
      <img src="/assets/img/highlights/5.jpeg" alt="Electrical Club " onclick="enlargeImage(this)">
      <div class="text">A final photo marking a successful tenure as President of the Electrical Club, Pulchowk Campus</div>
    </div>
    <div class="slide">
      <img src="/assets/img/highlights/1.jpg" alt="Post Exam Hiking" onclick="enlargeImage(this)">
      <div class="text">Post Exam Hiking to Annapurna Base Camp</div>
    </div>
    <div class="slide">
      <img src="/assets/img/highlights/7.png" alt="Final Year Project" onclick="enlargeImage(this)">
      <div class="text">Late-night run of the thesis project before tomorrow's submission </div>
    </div>
     <div class="slide">
      <img src="/assets/img/highlights/8.jpeg" alt="Laapsi-AI" onclick="enlargeImage(this)">
      <div class="text"> Before Flight to Jumla for showcasing Laapsi-AI </div>
    </div>

  </div>



  <!-- Navigation buttons -->
  <a class="prev" onclick="changeSlide(-1)">&#10094; Previous</a>
  <a class="next" onclick="changeSlide(1)">Next &#10095;</a>
</div>

<!-- Enlarge Image Modal -->
<div id="modal" class="modal">
  <span class="close" onclick="closeModal()">&times;</span>
  <img class="modal-content" id="enlargedImage">
  <div id="caption"></div>
</div>

---

<style>
/* Slider styles */
.slider-container {
  width: 100%;
  overflow: hidden;
  position: relative;
  max-width: 900px;
  margin: auto;
}

.slider {
  display: flex;
  transition: transform 0.5s ease-in-out;
  width: 100%;
}

.slide {
  min-width: 33.33%;
  box-sizing: border-box;
  padding: 10px;
}

.slide img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  cursor: pointer;
}

.text {
  color: white;
  font-size: 17px;
  padding: 12px;
  text-align: center;
  background-color: rgba(0, 0, 0, 0.7);
  margin-top: 8px;
  border-radius: 5px;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  padding: 10px;
  color: white;
  font-size: 18px;
  background-color: rgba(0, 0, 0, 0.3); /* More subtle background */
  border-radius: 3px;
  z-index: 1;
}

.prev {
  left: 0;
}

.next {
  right: 0;
}

.prev:hover, .next:hover {
  background-color: rgba(0, 0, 0, 0.5); /* More subtle hover */
}

/* Modal (for enlarged image) styles */
.modal {
  display: none;
  position: fixed;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
}

.modal-content {
  margin: auto;
  display: block;
  max-width: 80%;
  max-height: 80%;
  object-fit: contain; /* Maintain aspect ratio */
}

.modal-content, .close {
  animation: fadeIn 0.5s;
}

@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity: 1;}
}

.close {
  position: absolute;
  top: 20%;
  left: 100px; /* Move close button to the left side of the image */
  transform: translateY(-50%); /* Vertically center the button */
  color: white;
  font-size: 90px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover {
  color: #bbb;
}

This change will position the close button to the left of the image, vertically centered. You can tweak the left value further if needed to move the button closer or further from the image.

Let me know if you'd like further adjustments!


#caption {
  text-align: center;
  color: white;
  font-size: 20px;
  padding: 10px;
}
</style>

<script>
let slideIndex = 0;

function showSlides() {
  let slider = document.querySelector('.slider');
  let totalSlides = document.querySelectorAll('.slide').length;
  let slidesVisible = 3;
  let totalScrollWidth = slider.scrollWidth;
  let maxIndex = totalSlides - slidesVisible;

  if (slideIndex > maxIndex) {
    slideIndex = 0;
  } else if (slideIndex < 0) {
    slideIndex = maxIndex;
  }
  
  let offset = (totalScrollWidth / totalSlides) * slideIndex;
  slider.style.transform = 'translateX(' + (-offset) + 'px)';
}

// Automatically switch slides every 5 seconds
setInterval(function() {
  changeSlide(1);
}, 4500);

// Change slide manually using the buttons
function changeSlide(n) {
  slideIndex += n;
  showSlides();
}

// Enlarge image in a modal
function enlargeImage(img) {
  const modal = document.getElementById("modal");
  const modalImg = document.getElementById("enlargedImage");
  const captionText = document.getElementById("caption");

  modal.style.display = "block";
  modalImg.src = img.src;
  captionText.innerHTML = img.alt;
}

// Close the modal
function closeModal() {
  const modal = document.getElementById("modal");
  modal.style.display = "none";
}
</script>
