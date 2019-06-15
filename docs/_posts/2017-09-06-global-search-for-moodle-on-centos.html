---
layout: post
title: Global Search for Moodle on Centos
date: 2017-09-06 15:54:42.000000000 +01:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- code
- Development
- education
- Technology
tags:
- '3.3'
- '7.0'
- CentOS
- edTech
- Moodle
- PHP
meta:
  _wpcom_is_markdown: '1'
  _edit_last: '1'
  _thumbnail_id: '2720'
  _publicize_twitter_user: "@cullaloe"
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1560320659;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:3053;}i:1;a:1:{s:2:"id";i:678;}i:2;a:1:{s:2:"id";i:2816;}}}}
  _wpas_done_all: '1'
author:
  login: admin
  email: admin@cullaloe.net
  display_name: Nick
  first_name: Nick
  last_name: Hood
permalink: "/blog/2017/09/06/global-search-for-moodle-on-centos/"
---
<p><a href="https://cullaloe.com/files/2017/09/Screen-Shot-2017-09-06-at-16.11.59.png"><img class="alignright size-full wp-image-2716" src="{{ site.baseurl }}/assets/Screen-Shot-2017-09-06-at-16.11.59.png" alt="" width="371" height="90" /></a>My students are using a Moodle VLE to access resources and teaching materials and it became evident that some kind of global search function would help them find things quickly, especially later in the programme when they come to write their assignments.</p>
<p>I'm running Moodle on a CentOS 7.3 virtual private server with Plesk Onyx. The server hosts several other sites running WordPress, bespoke PHP and some other bits and pieces including the usual mail services. Some of the containers require the OS-standard PHP5.4 but a recent upgrade to Moodle 3.3 required me to switch the container to PHP 7.0.</p>
<p>Installing Global Search was a little tricky because of the multiple PHP versions running on the server, but I eventually figured it out to these key steps:</p>
<p><strong>Install the Solr Server</strong></p>
<pre>$ cd /opt
$ wget http://apache.mirrors.nublue.co.uk/lucene/solr/6.6.0/solr-6.6.0.tgz
$ tar zxvf solr-6.6.0.tgz
$ cp solr-6.6.0/bin/install_solr_service.sh .
$ rm -rf solr-6.6.0
$ ./install_solr_service.sh solr-6.6.0.tgz
$ chkconfig solr on
$ su - solr -c "/opt/solr/bin/solr create_core -c moodle"</pre>
<p>You should be able to visit <code>http://your-domain.tld:8983</code> to verify the Solr server is running OK.</p>
<p><strong>Secure the Solr Server</strong></p>
<p>By default, Solr is open to the world. You might want to secure it by adding this at the end of <code>/opt/solr/server/etc/webdefault.xml</code>:</p>
<pre class="p1"><span class="s1"><span class="Apple-converted-space">  </span>&lt;security-constraint&gt;</span>
<span class="s1"><span class="Apple-converted-space">   </span>&lt;web-resource-collection&gt;</span>
<span class="s1"><span class="Apple-converted-space">       </span>&lt;web-resource-name&gt;Solr Administration&lt;/web-resource-name&gt;</span>
<span class="s1"><span class="Apple-converted-space">       </span>&lt;url-pattern&gt;/*&lt;/url-pattern&gt;</span>
<span class="s1"><span class="Apple-converted-space">   </span>&lt;/web-resource-collection&gt;</span>
<span class="s1"><span class="Apple-converted-space">   </span>&lt;auth-constraint&gt;</span>
<span class="s1"><span class="Apple-converted-space">       </span>&lt;role-name&gt;solr-admin&lt;/role-name&gt;</span>
<span class="s1"><span class="Apple-converted-space">   </span>&lt;/auth-constraint&gt;</span>
<span class="s1"><span class="Apple-converted-space">  </span>&lt;/security-constraint&gt;</span>

<span class="s1"><span class="Apple-converted-space">  </span>&lt;login-config&gt;</span>
<span class="s1"><span class="Apple-converted-space">   </span>&lt;auth-method&gt;BASIC&lt;/auth-method&gt;</span>
<span class="s1"><span class="Apple-converted-space">   </span>&lt;realm-name&gt;Solr Administration&lt;/realm-name&gt;</span>
<span class="s1"><span class="Apple-converted-space">  </span>&lt;/login-config&gt;</span></pre>
<p>Create a file in the same directory called realm.properties containing your chosen authentication details (matching the role above) in a single line:</p>
<pre>admin: password, solr-admin</pre>
<p>Finally, add this just before the last line in jetty.xml in the same directory:</p>
<pre>&lt;Call name="addBean"&gt;
 &lt;Arg&gt;
  &lt;New class="org.eclipse.jetty.security.HashLoginService"&gt;
    &lt;Set name="name"&gt;Solr Administration&lt;/Set&gt;
    &lt;Set name="config"&gt;&lt;SystemProperty name="jetty.home" default="."/&gt;/etc/realm.properties&lt;/Set&gt;
    &lt;Set name="refreshInterval"&gt;0&lt;/Set&gt;
  &lt;/New&gt;
 &lt;/Arg&gt;
&lt;/Call&gt;</pre>
<p><strong>Install the PHP Solr Extension</strong></p>
<pre class="p1"><span class="s1">$ rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm</span>
<span class="s1">$ rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm</span>
<span class="s2">$ yum install libxml2-devel pcre-devel libcurl-devel php70w-devel php70w-pear
</span></pre>
<p>You'll need to build the extension using the right versions of phpize and php-config for your version of PHP, in my case, 7.0:</p>
<pre>$ cd /opt
$ curl -O https://pecl.php.net/get/solr-2.4.0.tgz
$ tar zxvf solr-2.4.0.tgz
$ cd solr-2.4.0/
$ ../plesk/php/7.0/bin/phpize
$ ./configure --with-php-config=/opt/plesk/php/7.0/bin/php-config
$ make
$ make install
$ cp /opt/solr-2.4.0/modules/solr.so /opt/plesk/php/7.0/lib64/php/modules/
$ sudo service httpd restart</pre>
<p>Visit the Site administration / ▶︎ Plugins / ▶︎ Search / ▶︎ Manage global search page in your Moodle installation to configure, index and enable the Solr Search Engine.</p>
<p>I am impressed with how quickly this has been used and appreciated by the students.</p>
