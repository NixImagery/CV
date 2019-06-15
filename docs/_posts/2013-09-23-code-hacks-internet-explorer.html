---
layout: post
title: 'Code hacks: Internet Explorer Compatibility mode'
date: 2013-09-23 20:21:00.000000000 +01:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Technology
tags:
- ".htaccess"
- browser
- compatibility
- IE
- Linux
- mode
- standards
- wordpress
meta:
  _wpas_done_all: '1'
  dsq_thread_id: '1790447264'
  _edit_last: '1'
  Views: '827'
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1559969674;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:3377;}i:1;a:1:{s:2:"id";i:1413;}i:2;a:1:{s:2:"id";i:678;}}}}
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2013/09/23/code-hacks-internet-explorer/"
---
<p><a href="http://cullaloe.com/files/2013/09/guess-browser.jpg"><img class="alignright  wp-image-765" style="margin-left: 2px; margin-right: 2px;" alt="guess-browser" src="{{ site.baseurl }}/assets/guess-browser.jpg" width="165" height="610" /></a>I've been developing a site for a national competition to be launched in October and ran into a little difficulty with Internet Explorer. Despite this browser losing ground amongst even the unthinking default user community, it is still sufficiently popular that I needed to look at the problem.</p>
<p>The site is running Wordpress on a LAMP server using <a href="http://kovshenin.com/" target="_blank">Konstantin Kovshenin</a>'s <a href="http://wordpress.org/themes/expound" target="_blank">Expound</a> theme. One of the testers noticed the letters "Ski" next to the Home menu item. Mousing over it produces a fleeting grey box to appear top left of the browser window. This turned out to be only visible in IE8, IE9 and IE 10 in "compatibility mode", a feature of IE that allows the browser to render sites that are broken by IE's shockingly poor implementation of standards, using a model from an earlier version. It's what a code monkey might call a Kludge.</p>
<p><a href="http://cullaloe.com/files/2013/09/Ski.png"><img class="alignleft  wp-image-767" style="margin-left: 2px; margin-right: 2px;" alt="Ski" src="{{ site.baseurl }}/assets/Ski.png" width="139" height="85" /></a>The "Ski" is in fact, the first few letters of "Skip to content". It is one of several features of the site's theme implementation which are broken in IE's compatibility mode.</p>
<p>There are several suggestions in the forums designed to force IE into non-compatibility mode and render the site properly. Most rely on delivering a &lt;Doctype&gt; tag on the very first line, followed immediately by a X-UA-Compatible meta tag. Unless this tag is placed on the line immediately after the Doctype tag, IE ignores it.</p>
<p>I considered trying to knock up a plugin to make this work in some kind of customisable way. Editing the theme's header.php file seemed doomed to be overwritten on the next update, and branching a child theme felt like too much hard work for such a small fix to accommodate a browser that I personally would like everyone to stop using. Part of me wants all sites to look broken when viewed with IE so as to encourage the masses to make an intelligent choice for once. Let's not start talking about democracy.</p>
<p>Anyway, a little more digging found a really elegant solution which suited my particular needs from <a href="http://qorbani.com/" target="_blank">Reza Qorbani</a>, which is to use the .htaccess file to have the Apache server sniff the browser and send the metatag. This is what I finished up with:</p>
<pre>BrowserMatch MSIE best-standards-support
Header set X-UA-Compatible IE=edge env=best-standards-support</pre>
<p>It works a treat. Thanks, Reza!</p>
