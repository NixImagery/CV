---
layout: post
title: Wordpress network domain mapping fix
date: 2014-02-13 21:14:08.000000000 +00:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
- Technology
tags:
- blog
- broken
- domain
- mapping
- MU
- multisite
- plugin
- redirect
- subfolder
- wordpress
- wp-mu
meta:
  _thumbnail_id: '912'
  dsq_thread_id: '2262810606'
  _wpas_done_all: '1'
  _edit_last: '1'
  Views: '240'
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1560474177;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:1164;}i:1;a:1:{s:2:"id";i:815;}i:2;a:1:{s:2:"id";i:678;}}}}
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2014/02/13/wordpress-network-domain-mapping-fix/"
---
<p>I've just been on an interesting little journey that started last September when I discovered that some of the sites on one of my Wordpress networks had stopped working.</p>
<p>You might enjoy a little schadenfreude if I admit now that it was because I had a brilliant idea and did something stupid. I've posted details here in the hope that (a) if I do it again, I can find out how to fix it, and (b) if you've done it too, you're closer to the solution than I have been for the past six months. I've 'genericed' the details to help you map it to your own setup.<!--more--></p>
<h3>The network setup</h3>
<p>Wordpress installed in top level folder (/), originally stand-alone but converted it to <strong>subfolder</strong> MU and kept it pretty much up to date. As of today, version 3.8.1. Some plugins, nothing fancy or particularly relevant except <a href="http://wordpress.org/plugins/wordpress-mu-domain-mapping/" target="_blank">Donncha and co.'s WordPress MU Domain Mapping</a> plugin, installed in <strong>wp-content/plugins</strong> and network activated in accordance with the current installation instructions.</p>
<p>The first blog was set up as the 'network', let's call it <strong>firstblog.tld</strong>. Other blogs added and mapped thus: <strong>firstblog.tld/secondblog</strong> mapped to <strong>secondblog.tld</strong>; <strong>firstblog.tld/thirdblog</strong> mapped to <strong>thirdblog.tld</strong>; [and so on to] <strong>firstblog.tld/nthblog</strong> mapped to <strong>nthblog.tld</strong>.</p>
<p>I kept a couple of blogs which were not mapped to a domain under <strong>firstblog.tld</strong>, e.g. <strong>firstblog.tld/coolblog</strong> and <strong>firstblog.tld/hotblog</strong>.</p>
<h3>The brilliant idea</h3>
<p>I wanted to change the network so that it wasn't <strong>firstblog.tld</strong> any more. I wanted it to be  <strong>thirdblog.tld</strong>. All I had to do was edit the entries in the <strong>wp_site</strong>, <strong>wp_blogs</strong> and <strong>wp_domain_mapping</strong> tables.</p>
<h3>The stupid thing</h3>
<p>I edited the entries in the <strong>wp_site</strong>, <strong>wp_blogs</strong> and <strong>wp_domain_mapping</strong> tables.</p>
<h3>The result</h3>
<p>All of the mapped domains worked fine. I thought I was a genius. However, the non-mapped blogs stopped working. All I got was a <strong>404 - not found</strong> error, as if I'd tried to navigate to a non-existent blog, e.g. <strong>firstblog.tld/notablog</strong>.</p>
<h3>The attempts to fix it</h3>
<p>There's no point in detailing everything I did to try to fix this. Essentially, I went back into the database and put the tables back the way I thought they were. Notice the important words in that sentence, "I thought".</p>
<p>Six months of fiddling about with (and frankly, learning a lot about) .htaccess, wp-config.php, DNS, plugins, WordPress, Apache and internet WP forums got me nowhere.</p>
<p>Eventually, I had cause to set up a brand spanking new WP network and took the opportunity to study in detail the differences between the new (which worked properly) and the old (which didn't). I found the cause, and thereby the solution.</p>
<h3>The cause and the solution</h3>
<p>The domain mapping plugin does not like it if you try to map the network to a domain. If the network is installed at <strong>mynetwork.tld</strong> there will be an entry for this domain in the <strong>wp_blogs</strong> table, probably as blog ID 1. If there is also an entry for this domain in <strong>wp_domain_mapping</strong> then the <em>unmapped</em> subfolder sites will return <strong>404 - not found</strong>.</p>
<p>In hacking about with the tables (see "The stupid thing", above), I had introduced this error. All I had to do was delete the <strong>firstblog.tld</strong> entry from the <strong>wp_domain_mapping</strong> table, and all the non-mapped subfolder blogs started working.</p>
<h3>The outcome</h3>
<p>Amongst other things, I got my <a href="http://mrhood.net/cpdlog" target="_blank">CPD log</a> back. Note the irony.</p>
