---
layout: post
title:      "SASS Mixins"
date:       2020-08-14 21:50:38 +0000
permalink:  sass_mixins
---


Sass, a CSS preprocessor, is something I've found rather useful while working on my React project. It can be found here: 

https://sass-lang.com/

It's particularly nice to be able to create what in Sass is called a "mixin". As there are multiple components of my app that require similar styling, a mixin allows me reuse portions of CSS code over and over again without having to repeatedly retype them.

An example:

@mixin some-styling {
  width: 100px;
	height: 100px;
	opacity: 0.5;
}

.thing-1 {
  @include some-styling();
}

.thing-2 {
  @include some-styling();
}

In this example, after compiling the Sass (or in my case, scss), both classes thing-1 and thing-2 would have the styling inlclude in the mixin. 



