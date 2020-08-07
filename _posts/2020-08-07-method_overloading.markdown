---
layout: post
title:      "Method Overloading"
date:       2020-08-07 18:18:06 +0000
permalink:  method_overloading
---


Method overloading is the creation of multiple methods that have the same name, but a different number/type of paramaters. For instance:

public static int sum(int a, int b) {
   return a + b;
}

public static int sum(int a, int b, int c) {
   return a + b + c;
}

Both of those sample methods are viable in Java thanks to method overloading. It's a new, to me at least, concept that I haven't run into while studying programming before. I had always thought that every method needed to have its own individual name otherwise there would be an error in the code. 

However, I can see where it would be useful. A programmer wouldn't need to create multiple methods that do similar things with slightly different names like sumTwo or sumThree.
