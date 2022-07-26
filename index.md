---
title: CIS 7000 - Web3.0 Security - University of Pennsylvania
layout: default
img: sec.jpg
active_tab: main_page 
---

<div class="alert alert-info" markdown="1">
This course will be capped at 30 students. We welcome undergrads, Masters, and PhD students. Please answer the waitlist questions to join.
</div>


<!--
<div class="alert alert-info" markdown="1">
The course is done!  Please fill out this [end of semester survey](https://docs.google.com/forms/d/e/1FAIpQLSfYzkk9MD5WOda8WgUgXeDEDy06gUunApho2Me4nYoLXzgufQ/viewform?usp=sf_link) to give us feedback on how to improve the class next year.  If you loved the class, and would like to apply to be a TA, please fill out [this application](https://docs.google.com/forms/d/e/1FAIpQLSeGM7uegYNxf0pY6T2lOhMpUosnVnH3c1woZ10IcFJ18IKN-A/viewform?usp=sf_link).  If you'd like to volunteer for activities  with my research group you can [fill out this form](https://docs.google.com/forms/d/e/1FAIpQLScWgXblpIkADdO_K3PQIgm4LAGz0o-XEByPIVJg6_ObxZVAPQ/viewform).
</div>


<!-- Display an alert about upcoming quizzes -->
{% capture now %}{{'now' | date: '%s'}}{% endcapture %}
{% for module in site.data.modules %}
{% if module.quiz %}
{% for quiz in module.quiz %}
{% capture release_date %}{{module.start_date | date: '%s'}}{% endcapture %}
{% capture due_date %}{{quiz.due_date | date: '%s'}}{% endcapture %}
{% if release_date < now and due_date >= now %}
<div class="alert alert-info">
<a href="{{quiz.url}}">{{ quiz.title }}</a> has been released. It is due before {{ quiz.due_date | date: "%I:%M%p" }} on {{ quiz.due_date | date: "%A, %B %-d, %Y" }}.
</div>
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}
<!-- End alert for upcoming quizzes -->

<!-- Display an alert about upcoming homework assignments -->
{% capture now %}{{'now' | date: '%s'}}{% endcapture %}
{% for page in site.pages %}
{% if page.release_date and page.due_date %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% capture due_date %}{{page.due_date | date: '%s'}}{% endcapture %}
{% if release_date < now and due_date >= now %}
<div class="alert alert-info">
<a href="{{page.url}}">{{ page.title }}</a> has been released.  
{% if page.deliverables %}
The assignment has multiple deliverables.
<ul>
{% for deliverable in page.deliverables %}
<li>{{ deliverable.due_date | date: "%b %-d, %Y" }} - {{deliverable.description}}.</li>
{% endfor %}
</ul>
{% else %}
It is due before {{ page.due_date | date: "%I:%M%p" }} on {{ page.due_date | date: "%A, %B %-d, %Y" }}.
{% endif %}
</div>
{% endif %}
{% endif %}
{% endfor %}
<!-- End alert for upcoming homework assignments -->
 

 



<!--


<div class="alert alert-info" markdown="1">
R2D2 ***Extra Credit*** Assignments (late submission not allowed):
* [Robot Exercise 1: Using Python to Control R2D2](r2d2_assignments/hw1/homework1.html)
* [Robot Exercise 2: Robot Navigation](r2d2_assignments/hw2/homework2.html)
* [Robot Exercise 3: Flag Capture Game using a Minimax Algorithm](r2d2_assignments/hw3/homework3.html)
* [Robot Exercise 4: Commanding Robots with Natural Language](r2d2_assignments/hw4/homework4.html)

Extra Credit Bounty Items:
* ~~Get the Python API that we developed working on Windows~~ (solved by Hanbang with Raspberry Pi)
* Find a way to communicate the robot's gyroscopic sensor info back to Python
* Develop a Python collision detection protocol 
</div>

-->


### CIS 700 - Web3.0 Security

#### Overview

Mirroring the shift from desktop applications to Internet-based distributed applications that began over two
decades ago, computing stands at the cusp of another shift, from distributed to decentralized applications.
Such applications, commonly called smart contracts, are programs stored and executed on blockchains.
They hold the potential to streamline the management of digital assets in diverse use-cases with wide-ranging
economic and societal ramifications, including auctions, financial contracts, elections, trading
platforms, and permission management.


**How can we make smart contracts more secure, bug free, and trustworthy?** 
In this course, we will learn various techniques for program security and how they apply to the Web3.0 domain.
The fundamentals of this course have roots in program analysis, testing, and formal verification. 
The advent of Web3.0 provides an exciting new application for these techniques. 
Smart contracts often hold funds and are frequent surfaces of attack. 
The cost of a bug in the Web3.0 domain is often massive and difficult to revert. 
In this course we will learn the foundations of program analysis while getting hands on experience in finding bugs and verifying correctness of smart contracts. 

#### Prerequisites

- Programming experience: participated in a substantial coding project in Java or a similar language.
- Tools and environment: ability to independently build/run software tools on command line or in a container.
- Mathematical foundations: maturity to read and understand research papers.

#### Format
- *Lectures* will include technical details about standard program analysis techniques and their applications to smart contracts.  
- *Assignments* will be of one of the following types:
	- Develop, debug, test, and deploy smart contracts.
	- Manually expose various types of vulnerabilities in example smart contracts.
	- Use pratical analysis tools to expose those vulnerabilities automatically.
- *Final project* will account for half of the course's total credit. It will be one of the following types:
	- Implement a specific (i.e., provided by instructors) established technique/idea in the course's scope.
	- Adapt an existing technique from Web2.0 security to smart contracts and develop a prototype.
	- Develop and prototype a new technique for security analysis of smart contracts.
	- Envision a new application of program analysis (e.g., Web3 data analytics) and develop a prototype.
- *Guest lectures* will be delivered by experts in academia, startups, and industry research labs. 

