---
layout: post
category : work
tagline: "Basic Input/Output System"
tags : [redmond, microsoft, leap, os, lua]
---
{% include JB/setup %}

### What is an Operating System?

Modern computers come with firmware used to perform hardware initialization during the booting process called BIOS (Basic Input/Output System). What is firmware? It's permanent software programmed into a ROM (read-only memory). The BIOS tells the CPU (Central Processing Unit) to look for an installed operating system (OS). An operating system is a group of computer programs that allow the user to interact with a computer. Thanks Wikipedia.


The operating system allows a user to interact with the software and hardware of the computer. One of its main functions is to manage access to the CPU's resources. A simple CPU can only run one process, so the ordering of these tasks must be intelligent. 

### Process Scheduling

The answer to ordering these tasks is process scheduling. The end goal is to make a scheduling system that is both "efficient" and "fair". We want don't want our queue of tasks to grow too big (lots of stuff not getting run, sometimes referred to as starvation), but we also want to run higher priority tasks sooner. The is the high level concept for a priority queue. For one of our assignments, we were tasked (hehe) with creating an scheduling algorithm for a simple OS in Lua. None of us have used Lua. Not only were we jumping into an assignment with fairly foreign concepts, but we also had to learn Lua syntax on the fly.


We are still working on the assignment. Look for my next post to see how we actually implemented a solution. One concept we will probably implement is [Aging](https://en.wikipedia.org/wiki/Aging_(scheduling)#Example).


If you want to see what the base code looks like, check out this [repo](https://github.com/alex-wap/schedlua).

### What's Next?

Tomorrow, we will complete our priority queue scheduling algorithm and learn about Azure services.


### View from my Window

![window]({{ site.url }}/assets/images/2-15-17/window.jpg){: .img-responsive }


---
