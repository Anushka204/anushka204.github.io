---
layout: single
author_profile: true
permalink: /
---

<h1>👋 Hi, I'm Anushka Sharma</h1>

<h3 id="typing-text" style="color:#4CAF50;"></h3>
<style>
#typing-text::after {
  content: "|";
  animation: blink 1s infinite;
}

@keyframes blink {
  0% { opacity: 1 }
  50% { opacity: 0 }
  100% { opacity: 1 }
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function() {

  const roles = [
    "Full Stack Developer",
    "Cloud & DevOps Enthusiast",
    "Backend Engineer",
    "Data Analytics Explorer"
  ];

  let roleIndex = 0;
  let charIndex = 0;
  let typingElement = document.getElementById("typing-text");

  function typeEffect() {
    if (charIndex < roles[roleIndex].length) {
      typingElement.innerHTML += roles[roleIndex].charAt(charIndex);
      charIndex++;
      setTimeout(typeEffect, 80);
    } else {
      setTimeout(eraseEffect, 1500);
    }
  }

  function eraseEffect() {
    if (charIndex > 0) {
      typingElement.innerHTML = roles[roleIndex].substring(0, charIndex - 1);
      charIndex--;
      setTimeout(eraseEffect, 40);
    } else {
      roleIndex = (roleIndex + 1) % roles.length;
      setTimeout(typeEffect, 200);


