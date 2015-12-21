---
layout: post
title: Tags in Jekyll - Part 2
tags:
- jekyll
external-url: https://blog.brandonparsons.me/2015-using-tags-in-a-jekyll-blog-on-github-pages/
---
Revisited creating a [tags](http://idiotandrobot.com/blog/tags/) page for this blog. 
In the end settled on using the technique found [here](https://blog.brandonparsons.me/2015-using-tags-in-a-jekyll-blog-on-github-pages/).
Pretty straightforward, apart from having to correct all of the post tag formats from
```
tags: [tag1 tag2]
```
to 
``` 
tags:
 - tag1
 - tag2
```

Now it's just a case of adding hyperlinks to tags in posts.
