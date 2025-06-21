---
layout: single
title: "Home"
classes: wide
author_profile: false
permalink: /
---

<!-- Load Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  html { scroll-behavior: smooth; }

  body {
    background-color: #0f0f0f;
    color: #eee;
    font-family: 'Inter', sans-serif;
    background-image: url('https://www.transparenttextures.com/patterns/cubes.png');
    background-repeat: repeat;
    background-size: auto;
  }

  .hero-intro {
    text-align: center;
    padding: 5rem 1rem 3rem;
    background: linear-gradient(135deg, #1a1a1a 0%, #111 100%);
    border-radius: 18px;
    margin-bottom: 3rem;
    box-shadow: 0 4px 30px rgba(0,0,0,0.3);
  }

  .hero-intro img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 3px solid #666;
    margin-bottom: 1.2rem;
  }

  .typing {
    font-weight: 600;
    border-right: 2px solid #eee;
    animation: blink 0.8s step-end infinite;
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }

  .section-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
  }

  .card {
    background: #1d1d1d;
    color: #eee;
    border-radius: 16px;
    padding: 2rem;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4);
    min-width: 280px;
    max-width: 350px;
    flex: 1;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.5);
  }

  .card img {
    border-radius: 12px;
    margin-bottom: 1rem;
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .btn,
  .btn--inverse {
    display: inline-block;
    padding: 0.6rem 1.2rem;
    background-color: transparent;
    border: 2px solid #eee;
    color: #eee;
    border-radius: 8px;
    text-decoration: none;
    margin-top: 1rem;
    transition: background 0.2s ease, color 0.2s ease;
  }

  .btn:hover,
  .btn--inverse:hover {
    background-color: #eee;
    color: #111;
  }

  .fade-in {
    animation: fadeIn 1.4s ease-out;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }
</style>

<div class="hero-intro fade-in">
  <img src="/assets/images/your-photo.jpg" alt="Jake Bergeron">
  <h1 style="font-size: 2.5rem; margin-bottom: 0.5rem;">Hi, I'm Jake Bergeron</h1>
  <p style="font-size: 1.25rem; color: #ccc; margin-bottom: 1.5rem;">
    <span class="typing" id="typing-text">Solutions Engineer • DevSecOps • BJJ Nerd</span>
  </p>
  <p style="max-width: 720px; margin: 0 auto; font-size: 1.1rem; line-height: 1.6;">
    I build secure pipelines, simulate realistic attack data, and turn my home lab into a proving ground for everything I learn in tech and on the mats.
  </p>
</div>

<script>
  const text = [
    "Solutions Engineer",
    "DevSecOps Nerd",
    "Jiu-Jitsu Practitioner",
    "Home Lab Tinkerer",
    "Linux Advocate"
  ];
  let i = 0;
  setInterval(() => {
    document.getElementById("typing-text").textContent = text[i % text.length];
    i++;
  }, 2800);
</script>

---

## 🚀 What I’m Focused On

<div class="section-grid fade-in">

  <div class="card">
    <img src="https://source.unsplash.com/400x200/?technology,dark" alt="DevSecOps">
    <h3>🔐 DevSecOps in Action</h3>
    <p>Designing secure CI/CD workflows with tools like Semgrep, Syft, and GitLab to catch vulnerabilities before they ship.</p>
    <a href="/blog/" class="btn btn--inverse">Explore Blog</a>
  </div>

  <div class="card">
    <img src="https://source.unsplash.com/400x200/?server,rack" alt="Home Lab">
    <h3>🧪 Home Lab Stack</h3>
    <p>Proxmox, containers, scanners, and simulated threats — all running from a rig in the basement.</p>
    <a href="/resume/" class="btn btn--inverse">See Résumé</a>
  </div>

  <div class="card">
    <img src="https://source.unsplash.com/400x200/?bjj" alt="BJJ Mindset">
    <h3>🥋 BJJ x Engineering</h3>
    <p>Resilience, calm under pressure, and flow state — the same principles apply on the mat and in technical leadership.</p>
    <a href="/about/" class="btn btn--inverse">Learn More</a>
  </div>

</div>

---

## 📝 Latest Post

{% assign post = site.posts.first %}
### <a href="{{ post.url }}">{{ post.title }}</a>
<small>Posted on {{ post.date | date: "%B %d, %Y" }}</small>

{{ post.excerpt | markdownify }}

<a href="{{ post.url }}" class="btn btn--inverse">Read More →</a>

---

## 💬 Let’s Connect

Want to chat about secure pipelines, fly fishing in Maine, or how OSS is changing the security game?

[📬 Reach out](/contact/) or connect with me on [LinkedIn](https://linkedin.com/in/jakebergeron)

<div style="margin-top: 1.5rem;">
  <a class="btn btn--inverse" href="/contact/">Get in Touch</a>
</div>
