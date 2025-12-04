<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DDJDS Exhibition</title>
<style>
  body, html {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: Arial, Helvetica, sans-serif;
    scroll-behavior: smooth;
    background: black;
    color: white;
  }

  section {
    height: 100vh;
    width: 100%;
    padding: 80px 10%;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
    opacity: 0;
    transition: opacity 1.2s ease-out;
  }

  section.visible {
    opacity: 1;
  }

  h1 {
    font-size: 4rem;
    font-weight: 700;
    margin: 0 0 20px 0;
  }

  p {
    font-size: 1.2rem;
    max-width: 700px;
    line-height: 1.6;
  }

  .nav-dots {
    position: fixed;
    right: 30px;
    top: 50%;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: #666;
    cursor: pointer;
    transition: background 0.3s;
  }

  .dot.active {
    background: white;
  }

  .gallery-img {
    width: 60%;
    margin-top: 30px;
    border-radius: 6px;
  }
</style>
</head>
<body>

<div class="nav-dots">
  <div class="dot" onclick="scrollToSection(0)"></div>
  <div class="dot" onclick="scrollToSection(1)"></div>
  <div class="dot" onclick="scrollToSection(2)"></div>
  <div class="dot" onclick="scrollToSection(3)"></div>
  <div class="dot" onclick="scrollToSection(4)"></div>
  <div class="dot" onclick="scrollToSection(5)"></div>
  <div class="dot" onclick="scrollToSection(6)"></div>
  <div class="dot" onclick="scrollToSection(7)"></div>
  <div class="dot" onclick="scrollToSection(8)"></div>
  <div class="dot" onclick="scrollToSection(9)"></div>
</div>

<section id="one">
  <h1>Title/Digital Exhibition</h1>
  <p>Subtitle</p>
</section>

<section id="two">
  <h1>Gallery 1</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-1.jpg">
</section>

<section id="three">
  <h1>Gallery 2</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-2.jpg">
</section>

<section id="four">
  <h1>Gallery 3</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-3.jpg">
</section>

<section id="five">
  <h1>Gallery 4</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-3.jpg">
</section>

<section id="six">
  <h1>Gallery 5</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-3.jpg">
</section>

<section id="seven">
  <h1>Gallery 6</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-3.jpg">
</section>

<section id="eight">
  <h1>Gallery 7</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-3.jpg">
</section>

<section id="nine">
  <h1>Gallery 8</h1>
  <p>Blurb 1</p>
  <img class="gallery-img" src="your-image-3.jpg">
</section>

<script>
  // fade-in on scroll
  const sections = document.querySelectorAll("section");
  const dots = document.querySelectorAll(".dot");

  function revealSections() {
    sections.forEach((sec, i) => {
      const rect = sec.getBoundingClientRect();
      if (rect.top < window.innerHeight * 0.75) {
        sec.classList.add("visible");
        dots[i].classList.add("active");
      } else {
        dots[i].classList.remove("active");
      }
    });
  }

  function scrollToSection(i) {
    sections[i].scrollIntoView({ behavior: "smooth" });
  }

  window.addEventListener("scroll", revealSections);
  revealSections();
</script>

## </body>
## </html>
