---
layout: page
title: Ritzmond's Job Hunt Journey
id: home
permalink: /
---

<div class="hero-section">
  <h1>Welcome to My Professional Journey 👋</h1>
  <p class="tagline">Passionate Developer | Problem Solver | Continuous Learner</p>
</div>

<div class="journey-card">
  <h2>🎯 Current Goals</h2>
  <ul class="goal-list">
    <li>Seeking opportunities in Software Development</li>
    <li>Building impactful projects</li>
    <li>Growing my technical expertise</li>
  </ul>
</div>

<div class="skills-section">
  <h2>💻 Technical Arsenal</h2>
  <div class="skills-grid">
    <div class="skill-category">
      <h3>Languages</h3>
      <ul>
        <li>JavaScript/TypeScript</li>
        <li>Python</li>
        <li>Java</li>
      </ul>
    </div>
    <div class="skill-category">
      <h3>Frameworks</h3>
      <ul>
        <li>React</li>
        <li>Node.js</li>
        <li>Express</li>
      </ul>
    </div>
    <div class="skill-category">
      <h3>Tools</h3>
      <ul>
        <li>Git</li>
        <li>Docker</li>
        <li>AWS</li>
      </ul>
    </div>
  </div>
</div>

<div class="latest-updates">
  <h2>📝 Latest Updates</h2>
  <ul class="updates-list">
    {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
    {% for note in recent_notes limit: 3 %}
      <li class="update-item">
        <span class="update-date">{{ note.last_modified_at | date: "%Y-%m-%d" }}</span>
        <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
      </li>
    {% endfor %}
  </ul>
</div>

<div class="contact-section">
  <h2>📬 Let's Connect</h2>
  <p>I'm always open to discussing new opportunities and collaborations!</p>
  <div class="social-links">
    <a href="https://linkedin.com/in/your-profile" class="social-button">LinkedIn</a>
    <a href="https://github.com/your-profile" class="social-button">GitHub</a>
  </div>
</div>

<style>
  .wrapper {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem;
  }

  .hero-section {
    text-align: center;
    padding: 4rem 2rem;
    background: linear-gradient(135deg, #f5f7ff 0%, #e3e9ff 100%);
    border-radius: 15px;
    margin-bottom: 3rem;
  }

  .tagline {
    font-size: 1.2rem;
    color: #666;
    margin-top: 1rem;
  }

  .journey-card {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    margin-bottom: 3rem;
  }

  .goal-list {
    list-style-type: none;
    padding-left: 0;
  }

  .goal-list li {
    margin: 1rem 0;
    padding-left: 1.5rem;
    position: relative;
  }

  .goal-list li:before {
    content: "→";
    position: absolute;
    left: 0;
    color: #4a90e2;
  }

  .skills-section {
    margin-bottom: 3rem;
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
  }

  .skill-category {
    background: #f8f9fa;
    padding: 1.5rem;
    border-radius: 8px;
  }

  .skill-category h3 {
    color: #2d3748;
    margin-bottom: 1rem;
  }

  .skill-category ul {
    list-style-type: none;
    padding-left: 0;
  }

  .skill-category li {
    margin: 0.5rem 0;
    color: #4a5568;
  }

  .latest-updates {
    margin-bottom: 3rem;
  }

  .updates-list {
    list-style-type: none;
    padding-left: 0;
  }

  .update-item {
    display: flex;
    align-items: center;
    margin: 1rem 0;
    padding: 1rem;
    background: #f8f9fa;
    border-radius: 6px;
  }

  .update-date {
    color: #718096;
    margin-right: 1rem;
    font-size: 0.9rem;
  }

  .contact-section {
    text-align: center;
    padding: 3rem;
    background: #f5f7ff;
    border-radius: 10px;
  }

  .social-links {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .social-button {
    display: inline-block;
    padding: 0.8rem 1.5rem;
    background: #4a90e2;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    transition: background 0.3s ease;
  }

  .social-button:hover {
    background: #357abd;
  }

  h1, h2, h3 {
    color: #2d3748;
  }

  h2 {
    margin-bottom: 1.5rem;
  }

  .internal-link {
    color: #4a90e2;
    text-decoration: none;
  }

  .internal-link:hover {
    text-decoration: underline;
  }

  @media (max-width: 768px) {
    .skills-grid {
      grid-template-columns: 1fr;
    }
    
    .hero-section {
      padding: 2rem 1rem;
    }
    
    .wrapper {
      padding: 1rem;
    }
  }
</style>
