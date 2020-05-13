---
layout: single
title: Microarchitectural side-channel attacks
permalink: /side-channels/
classes: wide
---
Some highlights of previously published research projects and CPU
vulnerabilities discovered in our group (**note:** click on the logos to be
redirected to the website of the respective project).

<center>
<p>
  <a href="https://foreshadowattack.eu/">           <img src="/assets/img/foreshadow.svg" width="100" /></a>
  <a href="https://github.com/jovanbulck/sgx-step"> <img src="/assets/img/sgx-step.svg"   width="100" /></a>
  <a href="https://github.com/jovanbulck/nemesis"> <img src="/assets/img/nemesis.svg"     width="100" /></a>
  <a href="https://zombieloadattack.com/">         <img src="/assets/img/zombieload.svg"  width="100" /></a>
  <a href="https://plundervolt.com/">              <img src="/assets/img/plundervolt.svg" width="100" /></a>
  <a href="https://lviattack.eu/">                 <img src="/assets/img/lvi.svg"         width="100" /></a>
</p>
</center>

## Overview

![overview-img](/assets/img/tee-sca.png)
*Three types of enclave interactions for privileged adversaries: (1) pass
attacker-controlled arguments through the enclave interface; (2) derive execution
metadata during or after enclave invocation through side channels; (3) extract enclave
secrets from the CPU’s microarchitectural state through transient execution.*

So-called "microarchitectural" attacks
go beyond the visible architectural interface of the processor by exploiting
subtle, hidden details of the implementation of the underlying CPU (e.g.,
caches and branch predictors). 


## Videos

Find some introductory videos for some of our previous projects below.

<iframe width="584" height="328" src="https://www.youtube.com/embed/baKHSXeIIaI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/ynB1inl4G3c" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="1280" height="750" src="https://www.youtube.com/embed/yo9B2ZRVW9Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
