---
layout: post
title: CentOS 6.5 on MSWind
date: 2014-04-22 15:11:50.000000000 +01:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
- Development
- Technology
tags:
- '6.5'
- Advent
- CentOS
- Linux
- MSWind
- server
meta:
  _edit_last: '1'
  _wpas_done_all: '1'
  dsq_thread_id: '2630590920'
  Views: '343'
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1558878188;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:1094;}i:1;a:1:{s:2:"id";i:945;}i:2;a:1:{s:2:"id";i:2816;}}}}
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2014/04/22/centos-6-5-on-mswind/"
---
<p>Rather than make a pig's ear out of my live VPS by testing out new Ruby code I'm playing with, I thought it would be prudent to have a machine that I can break without upsetting users. I have an Atom-based Advent netbook which only ever gets played with occasionally and this afternoon, seems quite willing to volunteer for a rebuild as a CentOS server. The world loves a volunteer.<!--more--></p>
<p><a href="http://cullaloe.com/files/2014/04/photo.jpg"><img class="alignleft wp-image-1120 size-medium" src="{{ site.baseurl }}/assets/photo-e1398178086638-249x300.jpg" alt="photo" width="249" height="300" /></a></p>
<p>Why CentOS? Two main reasons, the first being that I host a number of websites and applications on a virtual private server (VPS) which runs the same operating system. It's about time I took my development safely offline. The second reason is that CentOS is very close to RedHat Enterprise Linux, in which I might do a certification over the summer. It wouldn't hurt me to have a sandbox.</p>
<p>The Advent doesn't have a CD/DVD drive but does sport USB and Ethernet ports, which meant that this process would be a net installation. This being the Google Age, I quickly found the idiot guide over at <a href="http://www.if-not-true-then-false.com/2011/centos-6-netinstall-network-installation/" target="_blank">if-not-true-then-false</a> (thank you, people). The steps are pretty straight forward and, on the assumption I'm going to need to build it again when I break it, are also summarised in this post, with the additional steps I needed to make the WiFi work.</p>
<p>On the Mac, download the net install image and burn it to a USB stick:</p>
<pre>mac:Downloads user$ <strong>ls</strong>
CentOS-6.5-i386-netinstall.iso
mac:Downloads user$ <strong>hdiutil convert -format UDRW -o CentOS-6.5-i386-netinstall.dmg CentOS-6.5-i386-netinstall.iso</strong> 
...
created: /Users/nick/Downloads/CentOS-6.5-i386-netinstall.dmg
mac:Downloads user$ <strong>diskutil list</strong>
... (plug in your USB here)
mac:Downloads user$ <strong>diskutil list</strong>
... (notice the address of the USB, /dev/disk3 in my case)
mac:Downloads user$ <strong>diskutil unmountDisk /dev/disk3</strong>
Unmount of all volumes on disk3 was successful
mac:Downloads user$ <strong>sudo dd if=CentOS-6.5-i386-netinstall.dmg of=/dev/rdisk3 bs=1m</strong>
Password:
...
mac:Downloads user$ <strong>diskutil eject /dev/disk3</strong></pre>
<p>Now boot the Advent from the USB stick and start the URL install. It requires the machine to be connected to the internet, which is done using an ethernet cable straight into the router. I chose:</p>
<pre>http://mirror.centos.org/centos/6.5/os/i386/</pre>
<p>as the mirror and made some custom package selections to give me the web/database server and development machine that I need. Once the process is complete, the machine reboots (you can take the USB stick out now) and there's just a little tidying up to do. I need this little machine to be able to connect over WiFi, which CentOS doesn't do out of the box, so had to establish the right driver and install it from <a href="http://elrepo.org/tiki/tiki-index.php" target="_blank">ElRepo</a> (follow the instructions there to set up your repositories):</p>
<pre>[user@advent ~]$ <strong>su
</strong>[user@advent ~]$ <strong>lspci -nn</strong>
... <em>lists your controllers, including wifi, notice [10ec:8199]:</em>
02:00.0 Network controller [0280]: Realtek Semiconductor Co., Ltd. RTL8187SE Wireless LAN Controller [10ec:8199] (rev 22)</pre>
<p>Now you can <a href="http://elrepo.org/tiki/DeviceIDs" target="_blank">go look up which driver</a> you need for your device ID pair. In my case, I needed kmod-rtl8187se for controller device [10ec:8199]. Take care to notice the 1's and the l's.</p>
<pre>[user@advent ~]$ <strong>yum install kmod-rtl8187se</strong></pre>
<p>Once you reboot, the module will be loaded and you can connect over WiFi and ditch the Ethernet cable. Once again, Robert is a relative.</p>
