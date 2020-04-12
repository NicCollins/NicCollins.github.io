---
layout: post
title:  "Virtual Easter Egg Hunt"
date:   2020-04-11 22:06:49 -0400
categories: tutorial javascript
---
For Easter I built a virtual easter egg hunt. This project was based around providing a way to "find" eggs in a spherical panorama.
The result of that project can be seen at this [link][egg-hunt-link].

In order to build the egg hunt I had to create a pair of spherical panoramas. That was done by first taking a sequence of pictures in a spherical pattern using my wife's camera. Once all the photos were taken they were imported into a tool called [Hugin][hugin-link] to genarate the panoramas.

The reasoning for two panoramas was to allow for more space to search for eggs as well as allowing for more eggs to be found as the same eggs could be used in both locations.

Once the panoramas had been generated they needed to be displayed in a webpage such that they could be interacted with. For this task [PhotoSphere Viewer][psv-link] was used as it provided both a way to display and move about, but also events. It is the event triggered on a double click that provided the ability to detect when an egg was found.

The final piece to bring it all together was the javascript needed to handle alerting when an egg was found. This relied on the previouslt mentioned double click event. The code used for detecting if an egg was found was also the code used to get the coordinated of the eggs originally. Once the egg is found the PhotoSphere Viewer also provides the ability to add markers to the panorama which marked found eggs.

To view the end result code you can find the GitHub repository [here][egg-hunt-gh].  
For a more in depth walk through see [here][egg-hunt-tutorial].

[egg-hunt-link]: http://mt-tabor-baptist-church-egghunt.s3-website-us-east-1.amazonaws.com/
[hugin-link]: http://hugin.sourceforge.net/
[psv-link]: https://photo-sphere-viewer.js.org/
[egg-hunt-gh]: https://github.com/NicCollins/virtual-easter-egg-hunt
[egg-hunt-tutorial]: https://niccollins.github.io/virtual-easter-egg-hunt/