---
layout: home
title: Natural Language Processing
nav_exclude: true
toc: true
seo:
  type: Courses
  name: Natural Language Processing
---

# {{ site.tagline }}
{: .no_toc .mb-2 }
{{ site.description }}
<br>
MoWe / 11:50am - 1:10pm	, [WEB L102](https://map.utah.edu/index.html?code=WEB), [Recordings](https://www.youtube.com/playlist?list=PLbuogVdPnkCrPZ4Vc-GRnk730SLhC1L43)
{: .fs-6 .fw-300 }

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign lead_ta = site.staffers | where: 'role', 'Lead TA' %}
{% for staffer in lead_ta %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'TA' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

---

Course description coming soon.

Through this **website** we will share:
* [Schedule](https://utah-intro-nlp.github.io/#calendar) & lecture materials (slides, recordings, readings)
* [FAQ before enrolling](https://utah-intro-nlp.github.io/#faq-before-enrolling)

Syllabus, announcements, communicating grades, policies, etc. are shared on **Canvas**. Communication will be done through **Piazza**. You will turn in your assignments to **Gradescope**. 

**The current page you are on is NOT the syllabus. Please review this syllabus carefully – students are responsible for understanding everything there!**

Many links on this website can be accessed only with your gcloud.utah.edu account.

## Calendar

The calendar and readings are **tentative** and **subject to change**. 

<table>
  <thead>
  <tr>
    <th>Date</th>
    <th>Theme</th>
    <th>Topic</th>
    <th>Lecture Materials</th>
    <th>Work due</th>
  </tr>
  </thead>
  <tbody>
  {% for week in site.data.calendar %}
    {% for day in week.days %}
      <tr>
        <td>{{day.date}}</td>
        <td class="cal-content">{{day.theme}}</td>
        <td class="cal-content">{{day.topics}}</td>
        <td class="cal-content">
          {% if day.recording %}
            <a href="{{day.recording}}" class="cal-content-link">[recording]</a>
          {% endif %}
          {% if day.slides %}
            <a href="{{day.slides}}" class="cal-content-link">[slides]</a>
          {% endif %}
          {% if day.readings %}
            <a href="{{day.readings}}" class="cal-content-link">[readings]</a>
          {% endif %}
        </td>
        <td class="cal-content">{{day.due}}</td>
      </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>

## FAQ Before Enrolling

{::options parse_block_html="true" /}

<details><summary markdown="span"><b>What will you learn in this course? </b> [Click to expand!]</summary>

TBD

</details>                   
<br/>

<details><summary markdown="span"><b>How will you be evaluated?</b> [Click to expand!]</summary>

Your performance in this course will be evaluated by:

* [programming homework assignments](https://drive.google.com/drive/folders/1rL_NBVbnnbDuewV-_WnslwlNXB5hFUgg?usp=sharing) (30%)
* [final project](https://drive.google.com/drive/folders/1vc4UddSTgBZroD542DOmX-I-QWaXUEj0?usp=sharing) (30%)
* midterm exam (20%)
* final exam (20%)
</details>                   
<br/>

<details><summary markdown="span"><b>Formal pre-requisites? Expected background?</b> [Click to expand!]</summary>    

The formal pre-requisite is C- or better in CS 3505.

This course is designed for computer science majors. We expect that you:
* ...are experienced with programming in Python – we won't be reviewing your your code directly and we expect you to figure out the implementation side on your own; we are here to help you with understanding concepts and translating ideas into pseudocode, 
* ...are comfortable with basic calculus, probability, and linear algebra, 
* ...have some familiarity with machine learning and deep learning, 
* ...can quickly pick up coding in [pytorch](https://pytorch.org/).

If you completed CS 5353/6353 (Deep Learning), CS 5350/6350 (Machine Learning), CS 6957 (NLP with Neural Networks), or CS 6966/5966 (Local Explanations for Deep Learning Models), we expect you will be able to keep up. 


**<span style="color: black;">My advice:</span>** If you are interested in the course, **give it a  try**. We will spend the first two weeks going over the background and have a graded programming assignment about it. If you struggle with the background concepts and the first homework, you can withdraw---students may drop a course within the first two weeks of a given semester without any penalties. 


**<span style="color: black;">Revisiting/polishing your knowledge.</span>** You can prepare by:

1. There are a ton of Python resources for people with some programming experience. Check them out [here](https://wiki.python.org/moin/BeginnersGuide/Programmers). My colleagues suggest these: [1](https://www.learnpython.org/), [2](https://diveintopython3.net/), [3](https://snakify.org/en/), and [4](https://runestone.academy/ns/books/published/thinkcspy/index.html?mode=browsing).

2. Math and machine learning basics are nicely covered in the first part of the [Deep Learning book](https://www.deeplearningbook.org/). Obviously, you can use the same book to familiarize yourself with deep learning.

3. [Deep Learning with PyTorch: A 60 Minute Blitz](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html) (highly recommended)

4. [Practical Deep Learning for Coders by Fast.ai](https://course.fast.ai/) (3: Neural net foundations; 5: From-scratch model, 13: Backpropagation & MLP, 14: Backpropagation)

5. [Getting started with NLP for absolute beginners](https://www.kaggle.com/code/jhoward/getting-started-with-nlp-for-absolute-beginners) is good to familiarize yourself a bit with NLP. During the semester we will use [huggingface](https://huggingface.co/course).

</details>                   
<br/>