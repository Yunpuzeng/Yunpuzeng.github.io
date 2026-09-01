---
layout: default
title: About
---

<nav class="site-nav">
  <a class="active" href="/">About</a>
  <a href="/research/">Research</a>
  <a href="/education/">Education</a>
  <a href="/publications/">Publications</a>
  <a href="/CV_Yunpu_Zeng_7_7.pdf" target="_blank">CV</a>
</nav>

## Hi, I'm Yunpu! 👋

I was born and raised in **Chengdu, China** — a city I will always associate with good food, a relaxed pace of life, and home. 🐼

I studied Industrial Engineering at **Sichuan University**, where I completed my bachelor's degree. After that, I moved from Chengdu to Atlanta to pursue my M.S. in Industrial Engineering at **Georgia Tech**. I enjoyed my time here enough to stay a little longer — I am now continuing my Ph.D. in Industrial Engineering at Georgia Tech.

These days, I spend a lot of my time building models, working with data, and thinking about healthcare problems. I am especially interested in healthcare operations, disease modeling, microsimulation, and using quantitative methods to better understand health and healthcare decisions.

But research is only one part of my life. When I am away from my laptop, you can usually find me painting, playing the piano, or occasionally building something with robotics. 🎨 🎹 🤖

<a class="cv-button" href="/CV_Yunpu_Zeng_7_7.pdf" target="_blank">
  📄 Curriculum Vitae
</a>

---

## Beyond Research ✨

I have always liked making things — sometimes with code, sometimes with hardware, and sometimes with a paintbrush.

### 🎨 Painting

Painting is one of my favorite ways to slow down and switch gears. It gives me a completely different kind of creative space from research — no models, no debugging, just colors, ideas, and whatever I feel like making that day.

<p class="gallery-hint">Scroll through some of my paintings — click one to take a closer look. ✨</p>

<div class="painting-strip">

  <button class="painting-thumb" type="button" data-full="/painting-1.JPG">
    <img src="/painting-1.JPG" alt="Painting by Yunpu Zeng">
  </button>

  <button class="painting-thumb" type="button" data-full="/painting-2.png">
    <img src="/painting-2.png" alt="Painting by Yunpu Zeng">
  </button>

  <button class="painting-thumb" type="button" data-full="/painting-3.png">
    <img src="/painting-3.png" alt="Painting by Yunpu Zeng">
  </button>

  <button class="painting-thumb" type="button" data-full="/painting-4.jpg">
    <img src="/painting-4.jpg" alt="Painting by Yunpu Zeng">
  </button>

  <button class="painting-thumb" type="button" data-full="/painting-5.png">
    <img src="/painting-5.png" alt="Painting by Yunpu Zeng">
  </button>

</div>


### 🤖 Robotics

I have also been interested in robotics for a long time. There is something especially satisfying about turning an idea into something you can actually build, test, and watch move.

<div class="robotics-photo">
  <img src="/robotic.JPG" alt="Robotics project by Yunpu Zeng">
</div>


### 🎹 Piano

I also enjoy playing the piano. It is one of my favorite ways to relax — especially after spending a little too much time staring at code or simulation results.

---

## Let's Connect

Always happy to connect about research, shared interests, or just something interesting. :)

<div class="contact-grid">
  <a href="https://github.com/Yunpuzeng" target="_blank">GitHub</a>
  <a href="https://orcid.org/0009-0004-7652-3358" target="_blank">ORCID</a>
  <a href="https://www.linkedin.com/in/yunpu-zeng-49568728a" target="_blank">LinkedIn</a>
  <a href="mailto:cicizeng412@gmail.com">Email</a>
  <a href="https://www.instagram.com/ci_zzyp/" target="_blank">Instagram</a>
</div>


<!-- Painting Lightbox -->

<div class="lightbox" id="painting-lightbox" aria-hidden="true">
  <button class="lightbox-close" type="button" aria-label="Close image">×</button>
  <button class="lightbox-prev" type="button" aria-label="Previous painting">‹</button>
  <img class="lightbox-image" src="" alt="Enlarged painting by Yunpu Zeng">
  <button class="lightbox-next" type="button" aria-label="Next painting">›</button>
</div>


<script>
(() => {
  const thumbnails = Array.from(document.querySelectorAll('.painting-thumb'));
  const lightbox = document.getElementById('painting-lightbox');

  if (!lightbox || !thumbnails.length) return;

  const image = lightbox.querySelector('.lightbox-image');
  const close = lightbox.querySelector('.lightbox-close');
  const previous = lightbox.querySelector('.lightbox-prev');
  const next = lightbox.querySelector('.lightbox-next');

  let currentIndex = 0;

  function showImage(index) {
    currentIndex = (index + thumbnails.length) % thumbnails.length;
    image.src = thumbnails[currentIndex].dataset.full;
  }

  function openLightbox(index) {
    showImage(index);
    lightbox.classList.add('open');
    lightbox.setAttribute('aria-hidden', 'false');
  }

  function closeLightbox() {
    lightbox.classList.remove('open');
    lightbox.setAttribute('aria-hidden', 'true');
    image.src = '';
  }

  thumbnails.forEach((thumbnail, index) => {
    thumbnail.addEventListener('click', () => openLightbox(index));
  });

  previous.addEventListener('click', (event) => {
    event.stopPropagation();
    showImage(currentIndex - 1);
  });

  next.addEventListener('click', (event) => {
    event.stopPropagation();
    showImage(currentIndex + 1);
  });

  close.addEventListener('click', closeLightbox);

  lightbox.addEventListener('click', (event) => {
    if (event.target === lightbox) closeLightbox();
  });

  document.addEventListener('keydown', (event) => {
    if (!lightbox.classList.contains('open')) return;

    if (event.key === 'Escape') closeLightbox();
    if (event.key === 'ArrowLeft') showImage(currentIndex - 1);
    if (event.key === 'ArrowRight') showImage(currentIndex + 1);
  });
})();
</script>
