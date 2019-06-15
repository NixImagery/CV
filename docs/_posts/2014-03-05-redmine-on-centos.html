---
layout: post
title: Redmine on CentOS
date: 2014-03-05 10:11:00.000000000 +00:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
tags:
- CentOS
- parallels
- project management
- rails
- ruby
- software
- VPS
meta:
  dsq_thread_id: '2363740400'
  _wpas_done_all: '1'
  _edit_last: '1'
  _thumbnail_id: '956'
  Views: '1309'
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1560332676;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:1117;}i:1;a:1:{s:2:"id";i:1094;}i:2;a:1:{s:2:"id";i:2816;}}}}
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2014/03/05/redmine-on-centos/"
---
<p>If you listened to that last audioboo, you'll maybe recognise that I like the idea that being in control of your destiny is connected to how much you know about your life. The podcast was talking about organisations but my life at the moment is not unlike an organisation, with projects, finance and time management all being features. I have been using a number of tools to track all of this activity and frankly they're not good enough, so I thought I'd give Redmine a try, after a couple of strong recommendations. Here's I how I set it up on my CentOS VPS (Virtual Private Server).<!--more--></p>
<h3>Install ruby</h3>
<p>First, check that ruby isn't already installed:</p>
<pre>[root@server ~]# ruby -v
-bash: ruby: command not found</pre>
<p>Next, get it over ftp, dropping it into a suitable folder:</p>
<pre>[root@server ~]# mkdir Downloads
[root@server ~]# cd Downloads/
[root@server Downloads]# ftp ftp.ruby-lang.org</pre>
<p>Login with username <strong>Anonymous</strong> (no password), find and download the current version (2.1.1 in my case):</p>
<pre>ftp&gt; cd /pub/ruby/stable
ftp&gt; get ruby-2.1.1.tar.gz
ftp&gt; bye</pre>
<p>Unpack and compile it on your local system (but see below about issues with openssl before doing this):</p>
<pre>[root@server Downloads]# tar xzvf ruby-2.1.1.tar.gz
[root@server Downloads]# cd ruby-2.1.1
[root@server ruby-2.1.1]# ./configure 
[root@server ruby-2.1.1]# make
[root@server ruby-2.1.1]# make install</pre>
<p>Now check it's there and the package manager for ruby (gem):</p>
<pre>[root@server ruby-2.1.1]# ruby -v
[root@server ruby-2.1.1]# gem -v</pre>
<p>This all worked for me, so I coule move to the next step. If you're following this and hit problems, check out the <a href="http://www.redmine.org/projects/redmine/wiki/Redmine_on_CentOS_installation_HOWTO" target="_blank">Redmine install guide</a>, which is what I have been following. Gem reports version 2.2.2 on my system at this point.</p>
<p>The application server module for Ruby in Apache is called passenger. Install it and restart Apache:</p>
<pre>[root@server ruby-2.1.1]# rpm --import http://passenger.stealthymonkeys.com/RPM-GPG-KEY-stealthymonkeys.asc
[root@server ruby-2.1.1]# yum install http://passenger.stealthymonkeys.com/rhel/6/passenger-release.noarch.rpm
[root@server ruby-2.1.1]# yum install mod_passenger
[root@server ruby-2.1.1]# service httpd restart</pre>
<h3>Quick fix: gem openssl problem</h3>
<p>There is a widely-reported problem with gem's ability to work properly. It complains, when attempting an install, thus:</p>
<pre>Unable to require openssl, install OpenSSL and rebuild ruby (preferred) or use non-HTTPS sources</pre>
<p>To take the latter hint (I already have openssl installed and don't have time to chase down the problem), you just need to add the http source and remove the https source:</p>
<pre>gem source -a http://rubygems.org/
gem source -r https://rubygems.org/</pre>
<h3>Install Redmine</h3>
<p>Now we have ruby installed, it's just a matter of getting the code suite and setting up a database in a similar way to setting up a wordpress install. I got the source from RubyForge:</p>
<pre>[root@server www]# wget http://rubyforge.org/frs/download.php/77242/redmine-2.4.0.tar.gz</pre>
<p>Untarring as before and moving the folder to the web-side, it's now just a matter of setting up a new database and user and editing the configuration file to point it at the right database. There will some gem dependencies to resolve and this was a pain to do but not difficult. Google is your friend - there's a lot of help out there on the forums. Give yourself an hour at the terminal to work through them, following the screen messages. The process involves editing the Gemfile and running bundler:</p>
<pre>[root@system redmine]# bundle install --without development test</pre>
<p>Those switches exclude the development and test environment dependencies as we're only interested in running a production version here.</p>
<h3>Openssl problem, again</h3>
<p>The persistence of the availability of openssl and the appropriate inclusion within the Ruby installation eventually forced me to dig deeper. There's no avoiding recompiling ruby from source with the right switches set. Begin by finding the openssl folder within the ruby source and executing this (yum only needed if you don't have openssl already):</p>
<pre># yum install openssl-devel.i686 openssl.i686
# cd /path/to/ruby_install_package/ext/openssl/
# ruby extconf.rb --with--openssl=/usr/bin/openssl --with--openssl-lib=/usr/lib/openssl</pre>
<p>There was a problem in the Makefile, however, so I had to add in a pointer to a missing header file, finding it first:</p>
<pre># sudo find / -name thread_native.h</pre>
<p>Then adding it just after the "topfile = " line in Makefile:</p>
<pre>top_srcdir = /root/Downloads/ruby-2.1.1</pre>
<p>Then run make and make install.</p>
<h3>Completing</h3>
<p>A few more things to run now. First, a secret key generator for session storage:</p>
<pre># rake generate_secret_token</pre>
<p>Create the database structure (at the command line) and populate the database with default configuration data:</p>
<pre># RAILS_ENV=production rake db:migrate
# RAILS_ENV=production rake redmine:load_default_data</pre>
<p>Create working directories and set permissions such that the application can write to them. Your installation will depend on how you configure your server but there is some help on the Redmine wiki <a href="http://www.redmine.org/projects/redmine/wiki/RedmineInstall" target="_blank">here</a> (look for "File System Permissions").</p>
<p>Testing is quite easy: ruby has a built-in web server which will respond to a command line invocation:</p>
<pre>[root@server redmine]# ruby script/rails server webrick -e production</pre>
<p>If all is hunky dory so far, you can visit port 3000 on your server in your favourite browser and see a Redmine homepage.</p>
<h3>Too many rubies</h3>
<p>You might find that you run into difficulty when you switch from the test webserver (webrick above) to running your ruby on rails application on apache. This for me was where most of the installation time went as I tried to figure out which ruby, which gems, which passenger: where to set the configuration was complex due to the numerous packages and applications are involved in this setup.</p>
<p>It has been a learning process for me but I got there in the end by paying close attention to error logs and keeping track of which settings I was making. It allowed me to diagnose where the issues were and resolve them. The last hurdle was overcome by removing a version of ruby I had installed with the yum package manager on my Centos server and reconfiguring the passenger module again:</p>
<pre>passenger-install-apache2-module</pre>
<p>The Phusion Passenger <a href="http://www.modrails.com/documentation/Users%20guide%20Apache.html" target="_blank">installation guide</a> was particularly helpful in sorting it out. I needed some final tweaks to the Apache configuration file to point at the right version of ruby and gem, and set up passenger. Once this was done, all I had to do was run the Centos virtual server reconfiguration script and restart the web server and Robert, apparently, is my mother's brother:</p>
<p><img class=" wp-image-957 alignnone" alt="redmine" src="{{ site.baseurl }}/assets/redmine1.png" width="542" height="331" /></p>
