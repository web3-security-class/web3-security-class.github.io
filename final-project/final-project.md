---
layout: default
img: eth-prism.webp
title: Final Project
active_tab: final-project
release_date: 2022-11-15
due_date: 2022-12-10 23:59:00EDT
materials:
---

<!-- Check whether the assignment is ready to release -->
{% capture today %}{{'now' | date: '%s'}}{% endcapture %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% if release_date > today %} 
<div class="alert alert-danger">
Warning: this assignment is under construction.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}
<!-- End of check whether the assignment is up to date -->


<!-- Check whether the assignment is up to date -->
{% capture this_year %}{{'now' | date: '%Y'}}{% endcapture %}
{% capture due_year %}{{page.due_date | date: '%Y'}}{% endcapture %}
{% if this_year != due_year %} 
<div class="alert alert-danger">
Warning: this assignment is out of date.  It may still need to be updated for this year's class.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}
<!-- End of check whether the assignment is up to date -->


<div class="alert alert-info">
This assignment is due on {{ page.due_date | date: "%A, %B %-d, %Y" }} before {{ page.due_date | date: "%I:%M%p" }}. 
</div>


{% if page.materials %}
<div class="alert alert-info">
You can download the materials for this assignment here:
<ul>
{% for item in page.materials %}
<li><a href="{{item.url}}">{{ item.name }}</a></li>
{% endfor %}
</ul>
</div>
{% endif %}




Final Project [100 points]
=============================================================

Final projects will be done in groups of 2-3 (depending on course size).


Final project ideas are likely to fall in one of the following categories:
1. Develop and prototype a new technique for security analysis of smart contract
2. Adapt existing technique from Web2.0 security to smart contracts and develop a prototype
3. Develop an idea for a new application of program analysis for Web 3.0 (e.g., analytics) and develop a prototype.
4. Implement a specific (i.e., provided by instructors) established (i.e., non-researchy) technique/idea in the course's scope.


