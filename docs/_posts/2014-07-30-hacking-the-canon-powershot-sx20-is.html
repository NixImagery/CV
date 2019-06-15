---
layout: post
title: Hacking the Canon Powershot SX20 IS
date: 2014-07-30 19:01:54.000000000 +01:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
- Technology
tags:
- Canon
- hacks
- Powershot
- SX20
meta:
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1560426220;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:1185;}i:1;a:1:{s:2:"id";i:328;}i:2;a:1:{s:2:"id";i:291;}}}}
  _edit_last: '1'
  _publicize_facebook_user: https://www.facebook.com/cullaloe
  _publicize_twitter_user: "@cullaloe"
  _thumbnail_id: '1225'
  _wpas_done_all: '1'
  Views: '2254'
  dsq_thread_id: '2886198671'
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2014/07/30/hacking-the-canon-powershot-sx20-is/"
---
<p>I've had my <a href="http://www.canon.co.uk/For_Home/Product_Finder/Cameras/Digital_Camera/PowerShot/PowerShot_SX20_IS/" target="_blank">Canon Powershot SX20 IS</a> camera for a few years now and have always regarded it as a stepping-stone to a better, "proper" camera. The problem is I have never quite got to the point where I can justify shelling out the considerable wonga to take the next step.</p>
<p>What I'd like is a modern digital equivalent to my brilliant old <a href="http://en.wikipedia.org/wiki/Nikon_FM" target="_blank">Nikon FM</a> that served me well for a number of years, with up to date features as well as the best of the old. Two things in particular have annoyed me about the SX20 - the maximum exposure time of 15 seconds and the digital compression which irrationally leaves me with <a href="http://en.wikipedia.org/wiki/Fear_of_missing_out" target="_blank">FOMO</a> - something is missing from my photographs.</p>
<p>Having resolved not to spend a grand on a new camera, instead I lobbed a hundred quid into the <a href="http://fundraise.unicef.org.uk/MyPage/Physics-Pixies-UNICEF-Appeal" target="_blank">Physics Pixies UNICEF appeal</a> and set about altering the camera I have to deal with the two "problems". The alterations amount to a firmware update using the CHDK (Canon Hack Development Kit) firmware addon. This is now an open-source project built on the work of programmer VitalyB's RAW enabler and Andrei Gratchev's development kit. The firmware update now includes a number of other really nice features including time-lapse, motion detection and bracketing of exposure and focus.</p>
<p><strong>Finding out the camera's firmware</strong></p>
<p>The <a href="http://en.wikipedia.org/wiki/Exchangeable_image_file_format" target="_blank">EXIF</a> data in a digital photograph tells you quite a lot about the camera that took it and the settings used - see, for example, <a href="https://www.flickr.com/photos/mrhood/10352576813/" target="_blank">this picture on Flickr</a>. Click "show EXIF". This tells me almost but not quite enough about the firmware Revision - 1.02 rev 2.00. Your camera will tell you, though. First, create an empty file called ver.req in the root of the SD card. I did this on a MacBook Pro with the SD card in a slot on the laptop by issuing these commands:</p>
<pre>$ cd Volumes/CANON_DC/
$ touch ver.req</pre>
<p>Put the card in your camera and start it up in playback mode. From the main screen (should be displaying NO IMAGE for no images on the card), press FUNC SET and DISP. buttons and the camera will display a screen like this for about 5 seconds:</p>
<p><a href="http://cullaloe.com/files/2014/07/IMG_4842.jpeg"><img class="aligncenter size-full wp-image-1218" src="{{ site.baseurl }}/assets/IMG_4842.jpeg" alt="IMG_4842" width="300" height="227" /></a></p>
<p>So my firmware version is GM1.02B. Other information is available - read <a href="http://chdk.wikia.com/wiki/FAQ#Q._How_can_I_get_the_original_firmware_version_number_of_my_camera.3F" target="_blank">the CHDK wiki</a> for more.</p>
<p><strong>Getting the firmware update</strong></p>
<p>There are lots of different versions of the CHDK available and it seems to be important that you get the right one. Visit the <a href="http://chdk.wikia.com/wiki/Downloads" target="_blank">download page</a> and click the link to the stable build - this takes you the list of available versions. Obviously, pick the right one for your camera - the SX20 files are near the end of the page. I went for this one:</p>
<pre><a href="http://mighty-hoernsche.de/bins/sx20-102b-1.2.0-3537-full.zip" target="_blank">sx20-102b-1.2.0-3537-full.zip</a></pre>
<p>I downloaded and unzipped the archive locally, then removed the quarantine tag from the binary (something the OSX archive utility does to protect you from yourself):</p>
<pre>$ xattr -d com.apple.quarantine DISKBOOT.BIN</pre>
<p><strong>Choosing the load method</strong></p>
<p>There are two possible methods to set up your camera with this new software, neither of which alters the camera's installed firmware. In the first and simplest, the SD card contains files that are loaded by the camera using the normal "firmware update" menu function. It doesn't actually update the firmware: the code is loaded into RAM which means that the camera reverts to standard operation when it is switched off.</p>
<p>The second method requires a "bootable" SD card containing the CHDK and partitioned in the right way - a slightly more complex procedure being required to set this up. I wanted to go with the first method initially, principally because I am impatient, but discovered (because the required PS.FIR file was missing from the download archive) that the <a href="http://chdk.wikia.com/wiki/SX20" target="_blank">SX20 CHDK does not support</a> the firmware update method. All the details for both methods are available <a href="http://chdk.wikia.com/wiki/Prepare_your_SD_card" target="_blank">on the wiki</a>.</p>
<p><strong>Preparing the SD card</strong></p>
<p>First step in preparing for the "bootable" method is to partition and format the SD card. I used the OSX disk utility to do this on an 8GB SD card, setting up a 500MB MBR partition and the rest in a second partition, both formatted as FAT. The disk utility seemed to throw an error after partitioning and didn't mount the first partition at this stage.</p>
<p>The next step requires the first partition to be unmounted anyway, as we convert it to a FAT16 partition by issuing this command using the appropriate disk identifier (disk1s1 in my case):</p>
<pre>$ sudo newfs_msdos -F 16 -v Canon_DC -b 4096 -c 128 /dev/disk1s1</pre>
<p>Ejecting and re-inserting the SD card shows the new partition arrangement is OK and both partitions mounted. The next step is to make the card bootable - first, by invoking the fdisk utility (you type the bold bits):</p>
<pre>$ <strong>sudo fdisk -e /dev/disk1</strong>
fdisk: could not open MBR file [] No such file or directory &lt;== IGNORE THIS
fdisk: 1&gt; <strong>setpid 1</strong>
Partition id ('0' to disable) [0 - FF]: [B] (? for help) <strong>1</strong>
fdisk:*1&gt; <strong>write</strong>
Device could not be accessed exclusively.
A reboot will be needed for changes to take effect. OK? [n] <strong>y</strong>
Writing MBR at offset 0.
fdisk: 1&gt; <strong>exit</strong></pre>
<p>Next, we have to edit the SD card's Master Boot Record. Get a copy of it locally by issuing this:</p>
<pre>$ sudo dd if=/dev/disk1s1 of=BootSector.bin bs=512 count=1</pre>
<p>Remember to use the correct disk identifier (disk1s1 in my case). If you get "Resource busy", it's because the first partition is mounted - unmount (do not eject) it and try the dd command again. Next, the BootSector.bin file needs to be edited - I used HexEdit.app - to overwrite from position 0x40 the word BOOTDISK:</p>
<p><a href="http://cullaloe.com/files/2014/07/bs.png"><img class="aligncenter size-medium wp-image-1222" src="{{ site.baseurl }}/assets/bs-300x244.png" alt="bs" width="300" height="244" /></a></p>
<p>You should finish up with a file that's still exactly 512 bytes that you can dd back to the SD card boot partition:</p>
<pre>$ sudo dd if=BootSector.bin of=/dev/disk1s1 bs=512 count=1</pre>
<p>Remounting the partition (using disk utility), the final step in preparing the SD card is to copy the CHDK files over. The file DISKBOOT.BIN (and PS.FI?, if you have it) goes in the first partition, everything else from the archive goes in the second, larger partition.</p>
<p><strong>Finally</strong></p>
<p>Eject the card and move the lock switch to the LOCK position (this is required to make CHDK operate - in the UNLOCK position, it's just a normal Powershot but limited to the first partition). Put the SD card in the camera and start it up - you'll notice a new splash screen:</p>
<p><a href="http://cullaloe.com/files/2014/07/IMG_1865.jpeg"><img class="aligncenter size-full wp-image-1225" src="{{ site.baseurl }}/assets/IMG_1865.jpeg" alt="IMG_1865" width="300" height="222" /></a></p>
<p>You'll also see some new items, like a battery monitor, but most of the CHDK functions are accessed through their own menus - you (and I) will have to spend a little time with <a href="http://chdk.wikia.com/wiki/CHDK_1.2.0_User_Manual" target="_blank">the user manual</a>, but look out for results on <a href="http://www.blipfoto.com/cullaloe" target="_blank">BlipFoto</a>, <a href="https://www.flickr.com/photos/mrhood/" target="_blank">Flickr</a> or maybe even <a href="http://500px.com/cullaloe" target="_blank">500px</a>.</p>
