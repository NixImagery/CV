---
layout: post
title: 'Code Hacks: Wordpress WP-Filebase Pro'
date: 2013-10-29 00:57:18.000000000 +00:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
tags:
- file download
- wordpress
- WP-Filebase
meta:
  dsq_thread_id: '1912616361'
  _edit_last: '1'
  _wpas_done_all: '1'
  Views: '1482'
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1559433318;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:945;}i:1;a:1:{s:2:"id";i:3377;}i:2;a:1:{s:2:"id";i:909;}}}}
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2013/10/29/code-hacks-wordpress-wp-filebase-pro/"
---
<p>I updated my Wordpress installations to 3.7 "Basie" this weekend and found that the file download stopped working for all users except admins. The files affected are those for which permissions are required (Subscriber and above).</p>
<p>I made a workaround to get it working for my physics teachers resource site at <a href="http://sptr.net" target="_blank">http://sptr.net</a>. In <em>classes/Item.php</em>, within function <em>CurUserCanAccess($for_tpl=false, $user = null)</em>, above the loop that checks user roles, you have to populate the roles array by calling <em>get_role_caps()</em>, thus:</p>
<pre>...
if(empty($frs)) return true; // item is for everyone!
$user-&gt;get_role_caps();
foreach($user-&gt;roles as $ur) { // check user roles against item roles
 if(in_array($ur, $frs))
 return true;
 }
...</pre>
<p>It looks like it's working for now. I've posted the fix to the <a href="http://wpfilebase.com/forums/topic/file-download-stops-working-with-version-3-1-11-wp-3-7/" target="_blank">Plugin support forum</a>.</p>
