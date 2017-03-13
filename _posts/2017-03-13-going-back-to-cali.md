---
layout: post
category : travel
tagline: "A natural dose of vitamin D"
tags : [california ]
---
{% include JB/setup %}

### CSS Tables

I don't enjoy writing CSS in general, but I encountered an interesting challenge at work. Without going into detail, I needed to build a mobile responsive group of elements. My original solution used Twitter Bootstrap's row divs to layout my elements. Eventually, I realized that my data was better displayed as a table.


After I refactored my elements into a table, I encountered another problem. As I resized the window, the elements would wrap and create an extra row of elements. My first row would be split into two rows, which was not what I wanted. I spent a bunch of time searching Bing (maybe it was on an "alternative search engine") for a solution. I ended up going with property I had never heard of: white-space. I used the table row selector `tr` and applied `white-space: nowrap;`. This solution stopped my rows from wrapping. Neat!


### Solution


Ultimately, I had to change my approach. My goal was to show the entire table and allow the user to zoom in as desired. The `tr{white-space: nowrap;}` solution clipped the end of the table from the screen and required scrolling to view. This is not a great user experience. I decided to scale each element using vw units (which is new in CSS3). What is a vw unit? 1 unit represents 1/100th of the viewport width. This unit is great for mobile responsive design because the width changes with the size of the viewport. Yay!


A quick note: a viewport is what a user can see on the screen. The viewport size varies depending on the user's device. The viewport will be smaller on a mobile phone versus a computer.


### My First VR Experience

I had extra time before an Amazon event, so I went to test out the Vive setup at the Microsoft store. I have used Google Cardboard before, but I do not consider it a full VR experience. My expectations were pretty high, but I was still impressed by how novel the experiences were. The store uses various demos to showcase the Vive. The first demo helps you visualize the amount of physical space you can use. It also helps you get familiar with the controllers. Here's a photo of me trying it out (thanks Tara):

![alex vive]({{ site.url }}/assets/images/3-8-17/vr.jpg){: .img-responsive .vertical }

#### Vesper Peak

The second demo I tried is called Vesper Peak. Here's a [YouTube video](https://www.youtube.com/watch?v=ebduy3C5pzA) of it if you're interested. It is a mountain landscape VR experience. You can skip to different locations using the controller and look around in all directions. At the edge of the cliff, I felt my legs wobble a little. This was the weakest demo I tried. There is nothing to show where your legs are and that took me out of the experience a bit. The resolution did not seem great, which was exacerbated by the stationary nature of the demo. I would also sometimes move my eyes to the edge of the Vive's lenses instead of moving my head, which also took me out of the experience.

#### Tilt Brush

Tilt Brush was my favorite demo. [Tilt Brush](https://www.tiltbrush.com/) is a 3D painting program by Google. I've spent many years designing things in 3D using traditional software such as Pro-Engineer, SolidWorks, and SketchUp. One weakness that these programs share is user interface. It is not a pleasant user experience and it takes a long time to figure things out. Tilt Brush, on the other hand, is incredibly intuitive. I was drawing the moment the program started up. It is really cool to be able to walk around and through your drawings. The resolution did not distract me in this context.

#### Raw Data

[Raw Data](http://store.steampowered.com/app/436320/) is a science fiction shooting game. As the player, you are constantly moving around. The movement prevents the resolution issues of the Vive from hampering the experience. I prefer the precise aiming of the mouse in first person shooting games, so I went into the demo a bit biased. It was fun, but it did not blow me away like Tilt Brush did.


### Next VR Experiences?

There are quite a few games on my list to try out. [Elite Dangerous](http://store.steampowered.com/app/359320/) is at the top. [The Lab](http://store.steampowered.com/app/450390/) is another demo I'm itching to try out. I don't have a rig powerful enough for VR, but my experience at the Microsoft Store makes me want to build one.

---
