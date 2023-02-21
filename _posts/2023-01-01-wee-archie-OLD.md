---
layout: post
title: Wee Archie
date: 2023-01-01 10:00
description: Resources
featured: 
published: false
tall-image: "images/wee-archie-tall.jpg"
image: "images/wee-archie.jpg"
categories: 
  - Activities
  - Hardware
---


Wee Archie is a suitcase-sized supercomputer designed and built to explain what a supercomputer is.

![image]({{ site.baseurl }}/images/wee-boy.jpg)
{:  style="width: 30%" 
alt="Wee Archie" 
title="Wee Archie"}

Wee Archie’s big brother, [ARCHER2](https://www.archer2.ac.uk) (link is external), takes up an entire building, with special floors to take its weight because it is so heavy. Find out more about Wee Archie from [this video](https://www.youtube.com/watch?v=5zmNE6czhYo) (link is external).



<div>

<iframe title="Video"  width="1000" height="560" src="https://www.youtube.com/embed/5zmNE6czhYo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

</div>

## How Wee Archie works

Wee Archie is constructed from 18 Raspberry Pi 2’s, a network switch, a power supply unit (PSU) and Ethernet cables.  Each Pi can calculate 93 million (that’s 93,000,000) instructions per second. Theoretically Wee Archie can therefore do 1,674,000,000 instructions per second if all of the Pi’s are used together at the same time!!

Wee Archie's big brother ARCHER has 4920 nodes, many network switches and its own special power supply from the power companies! ARCHER can calculate 1.6 x 1015 (1,600,000,000,000,000 or 16 followed by 15 zeroes!) instructions per second.

Each Pi has four cores, each capable of calculating, which can all see the same information, as they all reside on the same device. This is similar to your multicore laptop or phone: multiple processes run at the same time, allowing more than one thing to happen at once. Each core can see all the same information.

The nodes on ARCHER each have 24 cores. That means that ARCHER has a total of 118,080 cores.

16 of the Pi’s are ‘worker’ nodes, resulting in 16x4 (or 64) cores for any job to run on. To use all 64 cores we run a problem in ‘parallel’ so that we use parallel computing.

The final two Raspberry Pi’s are management nodes: they help us run the other 16 nodes, schedule jobs and allow us to interact with the ‘worker’ nodes.  This is the same as on a supercomputer where a person cannot interact directly with worker nodes, but instead submits jobs to be run on the supercomputer to the login or management nodes.

Addendum: you can find instructions on how to configure your very own [Raspberry Pi cluster here](https://epcced.github.io/wee_archlet/) (link is external).