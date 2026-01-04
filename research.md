---
layout: default
title: Research
---

<div class="section-header">
    <h1>Research</h1>
    <p class="section-description">Exploring the frontiers of AI, Security, and Decentralized Systems</p>
</div>

## Research Interests

My research spans several interconnected areas in computer science:

### Artificial Intelligence & Machine Learning

I investigate novel machine learning algorithms and their applications to real-world problems. My work focuses on developing interpretable and robust AI systems that can operate reliably in complex environments.

**Key topics:**
- Deep learning architectures
- Explainable AI (XAI)
- Automated machine learning (AutoML)

### Cybersecurity

Security is fundamental to modern computing systems. My research addresses emerging threats and develops proactive defense mechanisms using AI-driven approaches.

**Key topics:**
- AI-powered threat detection
- Privacy-preserving computation
- Secure system design

### Autonomous Big Data Analytics (AutoBDA)

As data continues to grow exponentially, there is a critical need for systems that can autonomously analyze and extract insights from massive datasets without extensive human intervention.

**Key topics:**
- Automated data pipeline construction
- Self-optimizing analytics systems
- Scalable processing frameworks

### Web3 & Blockchain Technologies

Decentralized technologies offer new paradigms for trust, transparency, and user sovereignty. I explore both the foundations and applications of these emerging systems.

**Key topics:**
- Smart contract security
- Decentralized identity
- Blockchain scalability solutions

---

## Current Projects

<!-- Edit this section or use _data/projects.yml -->

{% if site.data.projects %}
{% for project in site.data.projects %}
<div class="card">
    <h3 class="card-title">{{ project.title }}</h3>
    <p class="card-meta">{{ project.status }} | {{ project.funding }}</p>
    <p class="card-description">{{ project.description }}</p>
</div>
{% endfor %}
{% else %}

<div class="card">
    <h3 class="card-title">Project Title Here</h3>
    <p class="card-meta">Ongoing | Funding Source</p>
    <p class="card-description">Brief description of your research project. Edit this in research.md or add projects to _data/projects.yml for easier management.</p>
</div>

{% endif %}

---

## Research Group

I am fortunate to work with talented students and collaborators. If you are interested in joining my research group, please see the [Contact]({{ '/contact' | relative_url }}) page.

### Current Students

<!-- Add your students to _data/students.yml -->
{% if site.data.students %}
{% for student in site.data.students %}
- **{{ student.name }}** ({{ student.degree }}) - {{ student.topic }}
{% endfor %}
{% else %}
- Student names and research topics (edit in _data/students.yml)
{% endif %}

### Collaborators

- Collaborator names and affiliations (edit this section)
