---
layout: post
title:      "CSS Challenges"
date:       2020-08-21 23:16:56 +0000
permalink:  css_challenges
---


Who would have thought that creating a red 'x' without using text and positioning exactly where you want it with CSS would be so difficult?

For a practice app that I'm working on, I wanted to position a red 'x' over specific images. As I wanted the 'x' to go from one corner to another, just type 'x' in a <span> tag and then attempting to style it wouldn't do. After some online searching, I came up with the idea to create an empty div with a single top border.

The border was styled red, then I had to do some tinkering with with the position, left, top, width, and transform properties to get exactly what I wanted. 

The code ended up looking something like this:

```
.line {
   position: relative;
	 left: -300px;
	 top: 40px;
	 width: 255%;
	 transform: rotate(45deg);
}
```

After that, it required a second line with everything the same except for a -45deg rotation. Overall, I was happy with how it turned out.
