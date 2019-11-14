---
# Posts need to have the `post` layout
layout: post

# The title of your post
title: Sample Brain Game Project
image: assets/img/braingame/bmbg1.png
# This description is used to preview the page on search engines, social media, etc.
description: >
    A sample brain game made with Unity. This is a WebGL build that is deployed to the web and this site. Simple control and navigation to demostrate a grasp of Unity and controls.


# (Optional) Link to an image that represents your blog post.

# You can hide the description and/or image from the output
# (only visible to search engines) by setting:
# hide_description: false
# hide_image: false

# (Optional) Each post can have zero or more categories, and zero or more tags.
# The difference is that categories will be part of the URL, while tags will not.
# E.g. the URL of this post is <site.baseurl>/hydejack/2017/11/23/example-content/
categories: [gamedev]
tags: [gamedev, Unity2d, dev]
# If you want a category or tag to have its own page,
# check out `_featured_categories` and `_featured_tags` respectively.
---

#  Simple Brain Game
## Developing a brain game

![Game menu]({{ "assets/img/braingame/menu1.png" | absolute_url }})

### Game overview
- A simple game design with two main branching options of working out the left or right brain.


- Once selected each side will allow for different options.
- Currently the Left(Logic) side of the brain has a chess game. Currently only allowing a two player chess game (Working on AI but that coding is a bit of a challenge). I was really happy to code the full movement of pieces.

![Game menu]({{ "assets/img/braingame/menu2.png" | absolute_url }})

- Right (Creative) side is a color finding game where you must select a different color box in grid of color boxes. 

![Game menu]({{ "assets/img/braingame/menu3.png" | absolute_url }})

- The take away from this game is a persisten highscore

### Key take aways
- Menu navigation
- Sounds and persistent music and volume control
- PlayerPerf to save highscore

### Future Developemt
- This framework allows more games to be added and can be a general game navigational menu framework


 <!-- blank line -->
  <iframe src="https://ttruty.github.io/BrainGame.html" frameborder="1" allowfullscreen="true" width="1000" height="800"> </iframe>
<!-- blank line -->

### Acknowledgments
- Images and music was taken from royalty free open license archives
The main menu brain was edited from this artist [here](https://pxhere.com/en/photo/1370218)
- The music is from Kevin MacLean [here](https://incompetech.com/music/)