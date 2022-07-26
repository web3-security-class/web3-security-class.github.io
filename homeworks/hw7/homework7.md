---
layout: default
title: HW7 - Constraint Based Analysis with Gigahorse
active_tab: homework
release_date: 2022-11-02
due_date: 2022-11-08 23:59:00EDT

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



Homework 7: Constraint Based Analysis with Gigahorse [100 points]
=============================================================

{% comment %}
#### Learning Goals:
Gain an...
1. Ability to run and configurate a real static analysis tool to find bugs in smart contracts.
2. Understanding of the limitations of slither and an understanding of the limitations of static analysis.
3. Understanding of the benefits and utility of a static analysis tool.
<br>

{% endcomment %}

#### Suggested Readings
1. [Gigahorse: Thorough, Declarative Decompilation of Smart Contracts](https://yanniss.github.io/gigahorse-icse19.pdf)
2. [MadMax: Surviving Out-of-Gas Conditions in Ethereum Smart Contracts](https://dl.acm.org/doi/pdf/10.1145/3276486)

{% comment %}
## Instructions
For each of the deployed course smart contracts, attempt to find the vulnerability by running Slither. 
Use your knowledge of the vulnerabilities from the previous homeworks.
If Slither can't find the bug out of the box, don't give up! Attempt to edit the config file, or even transform the source of the smart contract.

For each of the contracts, report the following:
1. Did Slither find the bug? Y/N
    - If Yes:
        -  what was the time taken?
    - If No, why not? Is this a limitation of the Slither tool or a fundamental limitation of static analysis? 

2. List any modifications you made to the configuration or source, and report the effect.

<br>
### What to Submit 
1. PDF or text file with the report detailed above.
2. Answer the following short answer questions:  (Only 2-3 sentence response for each)
    - Why are the benefits and limitations of static analysis for finding bugs in smart contracts?
    - What bug oracles are used in Slither? What are some alternatives?
    - Were traces provided for the bugs found? Give some comment on why or why not

{% endcomment %}
