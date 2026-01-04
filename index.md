---
layout: default
title: Home
---

<section class="hero">
    <img src="{{ '/assets/images/profile.jpg' | relative_url }}" alt="{{ site.author.name }}" class="hero-image" onerror="this.src='https://via.placeholder.com/200x200?text=Photo'">
    <div class="hero-content">
        <h1>{{ site.author.name }}</h1>
        <p class="hero-title">{{ site.author.title }}</p>
        <p class="hero-affiliation">{{ site.author.department }}<br>{{ site.author.university }}</p>

        <div class="research-interests">
            {% for area in site.research_areas %}
            <span class="research-tag">{{ area }}</span>
            {% endfor %}
        </div>
    </div>
</section>

## About Me

I am an Associate Professor in the Department of Computer Science at UoA. My research focuses on the intersection of **Artificial Intelligence**, **Cybersecurity**, **Autonomous Big Data Analytics (AutoBDA)**, and **Web3 technologies**.

<!-- Edit the content below to personalize your bio -->

My work aims to develop intelligent systems that can autonomously analyze large-scale data while maintaining security and privacy. I am particularly interested in leveraging machine learning techniques to enhance cybersecurity measures and exploring the potential of decentralized technologies.

## Recent News

<!-- Add your news items to _data/news.yml -->
{% if site.data.news %}
<ul>
{% for item in site.data.news limit:5 %}
    <li><strong>{{ item.date }}</strong> - {{ item.content }}</li>
{% endfor %}
</ul>
{% else %}
- **2024** - Welcome to my academic website!
{% endif %}

## Selected Publications

<!-- This section automatically pulls from _data/publications.yml -->
{% if site.data.publications %}
{% for pub in site.data.publications limit:3 %}
<div class="publication">
    <p class="publication-title">{{ pub.title }}</p>
    <p class="publication-authors">{{ pub.authors }}</p>
    <p class="publication-venue">{{ pub.venue }}, {{ pub.year }}</p>
</div>
{% endfor %}

[View all publications &rarr;]({{ '/publications' | relative_url }})
{% endif %}
