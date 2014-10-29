---
layout: post
tags: [jekyll fontawesome]
---
[Jekyll Now](https://github.com/barryclark/jekyll-now) didn't include support for [Font Awesome](http://fontawesome.io/) icons so I ha(a?)cked them in by copying the method used by [Haacked](https://github.com/Haacked/haacked.com).

This requires a local copy of the font files and some @font-face configuration in the css:

```
@font-face {
    font-family: 'FontAwesome';
    src: url("/blog/font/fontawesome-webfont.eot");
    src: url("/blog/font/fontawesome-webfont.eot?#iefix") format("embedded-opentype"),url("/blog/font/fontawesome-webfont.woff") format("woff"),url("/blog/font/fontawesome-webfont.ttf") format("truetype"),url("/blog/font/fontawesome-webfont.svgz#FontAwesomeRegular") format("svg"),url("/blog/font/fontawesome-webfont.svg#FontAwesomeRegular") format("svg");
    font-weight: normal;
    font-style: normal;
```

This works brilliantly for *that version* of Font Awesome but goes wrong when you then try and reference a font from anewer version.

A whole range of methods are suggested on the Font Awesome [Get Started page](http://fontawesome.io/get-started/) and I'm using a variation of the first method suggested by referencing the BootstrapCDN css within my [style.scss](https://github.com/idiotandrobot/blog/commit/357395b8562872824a98f52cf99a5e5810a7ffc3) file.

`@import url("//maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css");`
