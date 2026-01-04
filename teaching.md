---
layout: default
title: Teaching
---

<div class="section-header">
    <h1>Teaching</h1>
    <p class="section-description">Courses and educational activities</p>
</div>

## Current Courses

<!-- Courses are loaded from _data/courses.yml -->

{% if site.data.courses %}
<div class="course-grid">
{% for course in site.data.courses %}
{% if course.current %}
<div class="card">
    <h3 class="card-title">{{ course.code }}: {{ course.name }}</h3>
    <p class="card-meta">{{ course.semester }} | {{ course.level }}</p>
    <p class="card-description">{{ course.description }}</p>
    {% if course.syllabus %}<a href="{{ course.syllabus }}">Syllabus &rarr;</a>{% endif %}
</div>
{% endif %}
{% endfor %}
</div>
{% else %}

<div class="course-grid">
    <div class="card">
        <h3 class="card-title">CS XXX: Course Name</h3>
        <p class="card-meta">Fall 2024 | Undergraduate</p>
        <p class="card-description">Course description here. Edit this in teaching.md or add courses to _data/courses.yml.</p>
    </div>
</div>

{% endif %}

---

## Past Courses

{% if site.data.courses %}
<div class="course-grid">
{% for course in site.data.courses %}
{% unless course.current %}
<div class="card">
    <h3 class="card-title">{{ course.code }}: {{ course.name }}</h3>
    <p class="card-meta">{{ course.semester }} | {{ course.level }}</p>
    <p class="card-description">{{ course.description }}</p>
</div>
{% endunless %}
{% endfor %}
</div>
{% endif %}

---

## Teaching Philosophy

<!-- Edit this section to reflect your teaching philosophy -->

I believe in creating an inclusive and engaging learning environment where students are encouraged to think critically and apply theoretical concepts to practical problems. My teaching approach emphasizes:

- **Hands-on learning** through projects and assignments
- **Real-world applications** connecting theory to practice
- **Collaborative work** fostering teamwork and communication skills
- **Continuous feedback** helping students improve throughout the course

---

## Student Resources

### Office Hours
- **Day/Time**: [Update in _config.yml or here]
- **Location**: [Your office location]
- **Virtual**: By appointment via email

### For Prospective Students

If you are interested in undergraduate or graduate research opportunities, please:

1. Review my [Research]({{ '/research' | relative_url }}) page
2. Read some of my recent [Publications]({{ '/publications' | relative_url }})
3. Send me an email with your CV and research interests

I am always looking for motivated students interested in AI, security, and emerging technologies.
