---
tags: 
- Jekyll 
- Font Awesome
---
[Jekyll Now](https://github.com/barryclark/jekyll-now) didn't include support for [Font Awesome](http://fontawesome.io/) icons so I ha(a?)cked them in by copying the method used by [Haacked](https://github.com/Haacked/haacked.com).

This requires a local copy of the font files and some @font-face configuration in the css:

{% gist aa02655ed20e0263f7f9 %}

This works brilliantly for *that version* of Font Awesome but goes wrong when you then try and reference an icon from a newer version.

A whole range of methods are suggested on the Font Awesome [Get Started page](http://fontawesome.io/get-started/) and I'm using a variation of the first method suggested by referencing the BootstrapCDN css within my [style.scss](https://github.com/idiotandrobot/blog/commit/357395b8562872824a98f52cf99a5e5810a7ffc3) file.

`@import url("//maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css");`

I'm not sure an external reference is better per se but it works for now.
