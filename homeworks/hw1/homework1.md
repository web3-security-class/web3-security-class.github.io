---
layout: default
img: solidity.jpeg
img_link: http://xkcd.com/353/
caption: Solidity - the smart contract programming language
title: Homework 1 - Programming in Solidity
active_tab: homework
release_date: 2022-09-07
due_date: 2022-09-20 23:59:00EDT
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


<!-- <div class="alert alert-info" markdown="span"> -->

Homework 1: Programming in Solidity [100 points]
=============================================================

In this assignment you will learn to program smart contracts in Solidity. 

#### Learning Goals:
In this assignment you will learn..
1. The basic syntax and semantics of the Solidity language
2. Creating an application which accepts, holds, and transfers ethereum
3. How to interact with our existing deployed course smart contract
4. How fork an Ethereum network
5. Navigating Hardhat framework 
6. Deploying your contract to an Ethereum test network

<br>

#### Warm up:
In this assignment, you will need to interact with our existing course contract. 
To test this interaction, you will need to fork the Ethereum test net. 

As a warm-up for these learning goals, complete the following exercise:
[Fork the F\*ing Ethereum Blockchain! Transfer tokens from Vitalik's Account ;)](https://medium.com/uv-labs/fork-the-f-ing-ethereum-blockchain-transfer-tokens-from-vitaliks-account-46d408f7356c)



<br>
### Instructions
Tbd..


