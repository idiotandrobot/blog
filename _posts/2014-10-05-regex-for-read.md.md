---
layout: post
title: RegEx for read.md
date: 2014-10-05 17:30 +0100
---
A regex to parse [read.md](https://github.com/idiotandrobot/blog/blob/gh-pages/read.md)

'\*{2}(?<Year>\d{4})\*{2}\r\n\r\n(?<Read>- \*{2}(?<Day>\d{1,2})-(?<Month>\w{3})\*{2} (?<Title>.*) by (?<Author>.*)\r\n)+'

