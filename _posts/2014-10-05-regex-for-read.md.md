---
layout: post
title: RegEx for read.md
date: 2014-10-05 17:30 +0100
---
A regex to parse [read.md](https://github.com/idiotandrobot/blog/blob/gh-pages/read.md)

`\*{2}(?&lt;Year&gt;\d{4})\*{2}\r\n\r\n(?&lt;Read&gt;- \*{2}(?&lt;Day&gt;\d{1,2})-(?&lt;Month&gt;\w{3})\*{2} (?&lt;Title&gt;.*) by (?&lt;Author&gt;.*)\r\n)+`

