---
layout: default
img: echidna.png
img_link: https://github.com/crytic/echidna
caption: The Echidna logo
title: Homework 3 - Fuzzing with Echidna
active_tab: homework
release_date: 2022-08-28
due_date: 2022-10-11 23:59:00EDT
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




Homework 3: Exploiting with Echidna [100 points]
=============================================================

#### Learning Goals:
Gain an...
1. Ability to run and configurate a real fuzzer to find bugs in smart contracts.
2. Understanding of the limitations of Echidna and an understanding of the limitations of randomized testing.
3. Understanding of the benefits and utility of a randomized testing tool.
<br>

#### Suggested Readings
1. [Echidna: Effective, Usable, and Fast Fuzzing for Smart Contracts](https://agroce.github.io/issta20.pdf)
2. [Randoop: Feedback-directed Random Test Generation](https://homes.cs.washington.edu/~mernst/pubs/feedback-testgen-tr125.pdf)

<br>
<br>

## Instructions
For each of the deployed course smart contracts, attempt to find the vulnerability by running Echidna. 
Use your knowledge of the vulnerabilities from the previous homework.
If Echidna can't find the bug out of the box, don't give up! Attempt to edit the config file, or even transform the source of the smart contract.

For each of the contracts, report the following:
1. Did Echidna find the bug? Y/N
    - If Yes:
        -  what was the time taken?
        -  list the transaction trace Echidna found to hit the bug. Was this the same way you manually exploited the bug in HW2?
    - If No, why not? Is this a limitation of the Echidna tool or a fundamental limitation of randomized testing? 

2. List any modifications you made to the config file or source, and report the effect.

<br>
### What to Submit 
1. PDF or text file with the report detailed above.
2. Answer the following short answer questions:  (Only 2-3 sentence response for each)
    - Why are fuzzers practical for bug finding?
    - What are the limitations of fuzzing?
    - How are bug finding traces minimized?
    - Give an example of one way bug equivalence classes defined. In other words, name one way to decide if multiple traces find the same bug.
    - What bug oracles are used in Echidna? What are some alternatives?
    - How are seeds selected?
    - How is the fuzzing guided?

