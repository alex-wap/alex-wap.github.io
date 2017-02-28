---
layout: post
category : work
tagline: "ambiguous specifications"
tags : [redmond, microsoft, leap, os, lua, window]
---
{% include JB/setup %}

### Operating Systems Part Two

We spent the entire day debugging and implementing the code for our task scheduler. Did my code work by the end of the day? **Nope**. What's the big takeaway? Code a crude solution early and spend time thinking about theory after it works. Other people presented their solutions (only one solution was fully implemented).


The major issue is dealing with high priority system tasks as well as user tasks. How do you avoid resource starvation (user tasks never run)?

### Implementations

#### Random Priority

This method treats all tasks the same way and uses one queue. Assign a random priority to the task. Then, randomly add it to the front of the queue or the end of the queue. This priority queue is mostly "fair" because it ensures that all tasks will be run and treated in a "random" way. 


What's the drawback? If you have a system task that is super important (like video/audio syncing), then you could have a huge delay and an extremely poor user experience.


How do you improve this random priority? You add some type of weighting system to make sure system tasks get a little extra boost.

#### 5:1 Ratio

This method uses two queues. One queue holds the super important system tasks. The other queue holds all the user tasks. Tasks are added to their respective queues in order, but there is a counter used to switch between the queues. Execute 5 system tasks, then execute 1 user task, and repeat the process.


The developer made his code slightly more efficient by checking if a queue is empty or not. This delays the need for counting and will just run tasks out of the non-empty queue.

#### Time Approach

This method uses one queue and adds a time property to each task. If a task is waiting a long time, important tasks will be put inserted after that task in the queue.


#### Time, Priority, and Frequency

This method uses a combination of the above methods and adds the concept of frequency. If a task has been run multiple times, it can be set with a lower priority. If the task is a resource hog (takes a long time to run without yielding), it can be run less frequently by lower its priority.


### Why?

Why did we use Lua to implement a task scheduler? The prompt was purposefully vague as a learning exercise. **What did we learn?**

* We worked with a brand new language
* We worked with a new code base
* We worked with a new code editor (Visual Studio)
* We learned new ways to debug 
* We learned that specifications can be vague and ambiguous
* We learned to code and implement early, even if it's inefficient


### TLDR

There is no perfect solution. All methods have pros and cons. Why do it? To learn a new language, work with a new code base, use Visual Studio, debug, and write code early.


### What's Next?

Tomorrow, we meet our teams and mentors.


### View from my Window

Looks just like yesterday. :(

![window]({{ site.url }}/assets/images/2-16-17/window.jpg){: .img-responsive }


### Bonus Photo - Microsoft Building 37

![halo reach]({{ site.url }}/assets/images/2-16-17/halo.jpg){: .img-responsive }


---
