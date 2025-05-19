---
layout: page
title: 31 Bridgewater St
permalink: /31-bridgewater-st
---

<div>
<a href="mailto:ben@wrth.me?subject=31%20Bridgewater%20St.">
<div class="info-box post-list">
    <p class="info-box-title">GET IN TOUCH</p>
    <p class="info-box-content">To enquire about this property, simply click this box to open your mail client. I will get back to you within 24 hours!</p>
</div>
</a>
</div>

This is a room 6 bed property located in the Baltic Triangle area of Liverpool City Centre! The property spans 5 floors, the middle 3 floors housing 2 bedrooms and a full size bathroom each. As well as this, there’s a whole floor for the open kitchen-living space complete with a Juliet balcony for views of the beautiful waterfront. Above that, there’s a private rooftop terrace that’s only accessible by members of the household.

I’m unfortunately leaving at the end of first year due to a career opportunity that has come up. I know all of the existing housemates well, and they’re a good group of people with varying tastes. If you’re someone who’d enjoy going out then prepare for some exciting nights! This property is also just a couple streets away from Kitchen St. so if you’re a fan of baseline you’re covered! Alternatively, there’s another subset of flatmates who enjoy having the night in a spending their time relaxing or keeping on top of assignments - and they’d enjoy your company too.

The house, along with many things around it, were built recently in a regeneration project that has seen the area become a beautiful hub for students. All surrounding properties are student houses and there’s a bakery and a brewery immediately across the small street this house is situated on.

There is a garage on the ground floor of this property and the option to get an on-street parking permit from the council is also available and can be used immediately outside the property.

Existing tenants are all male so bear this in mind when considering this property, however enquiries from all are welcome!

## Photo Bank

<div style="width:100%;height:100%;margin:0;padding:0;box-sizing:border-box;font-family:sans-serif;">
  <style>
    .gallery-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 5px;
      width: 100%;
      max-width: 100vw;
    }

    .gallery-container img {
      width: 100%;
      height: auto;
      display: block;
      cursor: pointer;
    }

    .overlay {
      position: fixed;
      top: 0; left: 0;
      width: 100vw;
      height: 100vh;
      background: rgba(0,0,0,0.9);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 9999;
      overflow: hidden;
    }

    .overlay img {
      max-width: 90vw;
      max-height: 90vh;
      transition: transform 0.3s ease;
    }
  </style>

  <div class="gallery-container">
    <img src="/assets/house/front.jpeg" onclick="showOverlay(0)">
    <img src="/assets/house/kitchen.jpeg" onclick="showOverlay(1)">
    <img src="/assets/house/living.jpeg" onclick="showOverlay(2)">
    <img src="/assets/house/terrace.jpeg" onclick="showOverlay(3)">
    <img src="/assets/house/bedroom.jpeg" onclick="showOverlay(4)">
    <img src="/assets/house/bathroom.jpeg" onclick="showOverlay(5)">
  </div>

  <div class="overlay" onclick="hideOverlay()" id="imgOverlay">
    <img id="overlayImg" src="">
  </div>

  <script>
    const images = [
        "/assets/house/front.jpeg",
        "/assets/house/kitchen.jpeg",
        "/assets/house/living.jpeg",
        "/assets/house/terrace.jpeg",
        "/assets/house/bedroom.jpeg",
        "/assets/house/bathroom.jpeg"
    ];

    let currentIndex = 0;

    function showOverlay(index) {
      currentIndex = index;
      document.getElementById('overlayImg').src = images[index];
      document.getElementById('imgOverlay').style.display = 'flex';
    }

    function hideOverlay() {
      document.getElementById('imgOverlay').style.display = 'none';
    }

    // Swipe support
    let startX = 0;

    document.getElementById('imgOverlay').addEventListener('touchstart', function(e) {
      startX = e.touches[0].clientX;
    });

    document.getElementById('imgOverlay').addEventListener('touchend', function(e) {
      const endX = e.changedTouches[0].clientX;
      const diffX = endX - startX;

      if (Math.abs(diffX) > 50) {
        if (diffX > 0) {
          // Swipe right - previous
          currentIndex = (currentIndex - 1 + images.length) % images.length;
        } else {
          // Swipe left - next
          currentIndex = (currentIndex + 1) % images.length;
        }
        document.getElementById('overlayImg').src = images[currentIndex];
      }
    });
  </script>
</div>

