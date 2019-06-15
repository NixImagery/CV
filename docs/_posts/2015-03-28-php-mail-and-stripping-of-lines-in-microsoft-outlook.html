---
layout: post
title: PHP Mail and stripping of lines in Microsoft Outlook
date: 2015-03-28 18:24:25.000000000 +00:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
- Development
tags:
- line breaks
- mail
- Microsoft
- Outlook
- PHP
meta:
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1560198182;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:1094;}i:1;a:1:{s:2:"id";i:1106;}i:2;a:1:{s:2:"id";i:2715;}}}}
  _publicize_twitter_user: "@cullaloe"
  _publicize_facebook_user: https://www.facebook.com/cullaloe
  Views: '112'
  dsq_thread_id: '3634851386'
  _wpas_done_all: '1'
  _edit_last: '1'
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2015/03/28/php-mail-and-stripping-of-lines-in-microsoft-outlook/"
---
<p>A client recently contacted me about problems with the formatting of messages he was getting from a php contact form on his site. He asked if I could insert a couple of CRLFs to make it easier to read and to stop it breaking the email links in the message.</p>
<p>The client's site is one of those creaking anachronistic beasts, from the days of hand-hacked HTML, which is full of things that work just well enough to enable him to concentrate on his business. I've been trying to get him to move to a CMS like WordPress for several years now, but he's not quite able to let go.</p>
<p>The contact form had not been a problem, as far as I knew, but all this while he has been putting up with messages from the site that look a bit like this:</p>
<blockquote><p>Name: FredEmail: <span style="text-decoration: underline;">fred@bloggs.comTel</span>: 09999899988Hi I was<br />
wondering blah blah blah blah?RegardsFred</p></blockquote>
<p>On my machines, they look like this:</p>
<blockquote><p>Name: Fred<br />
Email: fred@bloggs.com<br />
Tel: 09999899988<br />
Hi I was wondering blah blah blah blah?<br />
Regards<br />
Fred</p></blockquote>
<p>It seems that there is a "feature" that has existed in Microsoft Outlook since 2002, at least. What it does, often without letting the user know, is strip out any formatting of lines in the original message and replaces it with what it thinks you’d prefer. In text-only messages, this results in what you see in the first example above.</p>
<p>There’s a lot written about this, much of it along the lines of altering the user's practice to include workarounds that are only necessary because Microsoft can't write good code. See <a href="http://smallbusiness.chron.com/rid-double-spacing-outlook-74612.html" target="_blank">here</a>, for example, or <a href="http://www.webdeveloper.com/forum/showthread.php?144973-Plain-text-email-line-breaks-not-working" target="_blank">here</a> for one of the empirical solutions that suggests changing code to accommodate Outlook's perverse behaviour. Many <a href="http://stackoverflow.com/questions/22839027/phpmailer-ignoring-r-n" target="_blank">others</a> remain baffled. However, thanks to a bit of forensic inquiry by <a href="http://stackexchange.com/users/4344/mtruesdell" target="_blank">Matthew Truesdell</a>, there are some rules that can be interpreted in such a way that allows the php script to work for all users. Matthew posted the rules he found in Outlook 2007, over on <a href="http://stackoverflow.com/questions/136052/how-do-i-format-a-string-in-an-email-so-outlook-will-print-the-line-breaks/1638608#1638608" target="_blank">Stack Overflow</a>: I've adapted from those here, slightly, using the term "mode" to mean the behaviour of Outlook that strips out line breaks from plain text messages. Lines are assessed one at a time:</p>
<ul>
<li>Every message starts with the mode OFF.</li>
<li>Lines 40 characters or longer switch the mode ON.</li>
<li>Lines that end with a full stop (.), question mark (?), exclamation (!) or colon (:) switch the mode OFF.</li>
<li>Lines that turn the mode off will start with a line break, but will turn it back on if they are longer than 40 characters.</li>
<li>Lines that start or end with a tab turn the mode off.</li>
<li>Lines that start with 2 or more spaces turn the mode off.</li>
<li>Lines that end with 3 or more spaces turn the mode off.</li>
</ul>
<p>So it seems that one way to trick Outlook is to add 3 spaces at the end of each line, which in the code is just before the CRLF. I tried this, but be careful if you rely on it: different versions of Outlook do different things. Outlook 2013 is still stripping out the line breaks on the client machine, so we have this:</p>
<blockquote><p>Name: Fred   Email: <span style="text-decoration: underline;">fred@bloggs.com</span>   Tel: 09999899988<br />
Hi I was wondering blah blah blah blah?   Regards   Fred</p></blockquote>
<p>Which is still not satisfactory but at least allows him to click on the email address for a quicker response.</p>
<p>On my own machine (OSX Yosemite), Outlook 10 seems to be working as you'd expect, without interfering with the line breaks. Gmail works fine also. I think that's as far as I'm going to take it.</p>
