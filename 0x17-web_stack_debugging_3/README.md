# 0x17. Web Stack Debugging #3

## Overview
This project is part of the ALX System Engineering & DevOps curriculum. It involves debugging a web stack running a WordPress website on a LAMP (Linux, Apache, MySQL, and PHP) stack using `strace`, and automating the fix using Puppet.

## Project Details
- **Project Start**: Jun 18, 2024, 6:00 AM
- **Project Deadline**: Jun 24, 2024, 6:00 AM
- **Weight**: 1
- **Mandatory Tasks**: 1
- **Auto QA Review**: 0.0/2 mandatory

## Concepts
This project covers the following concepts:
- Web Server
- Web Stack Debugging

### Background Context
When debugging web applications, logs may not always provide sufficient information. Sometimes, deeper inspection using tools like `strace` is necessary. WordPress, a widely-used content management system, runs on a LAMP stack. Debugging this stack is a valuable skill for a SysAdmin.

## Requirements
### General
- All files will be interpreted on Ubuntu 14.04 LTS.
- Files must end with a new line.
- A `README.md` file at the root of the project directory is mandatory.
- Puppet manifests must pass `puppet-lint` version 2.1.1 without errors.
- Puppet manifests must run without error.
- The first line of Puppet manifests must be a comment explaining the manifest's purpose.
- Puppet manifest files must have the `.pp` extension.
- Files will be checked with Puppet v3.4.

### Installing `puppet-lint`
```bash
$ apt-get install -y ruby
$ gem install puppet-lint -v 2.1.1
```

## Task
### 0. Strace is your Friend
**Score: 0.0%**

Using `strace`, identify why Apache is returning a 500 error. After identifying and fixing the issue, automate the fix using Puppet.

#### Hints
- `strace` can attach to a running process.
- Use `tmux` to run `strace` in one window and `curl` in another.

#### Requirements
- The `0-strace_is_your_friend.pp` file must contain Puppet code.
- You can use any Puppet resource type for the fix.

#### Example
```bash
root@e514b399d69d:~# curl -sI 127.0.0.1
HTTP/1.0 500 Internal Server Error
Date: Fri, 24 Mar 2017 07:32:16 GMT
Server: Apache/2.4.7 (Ubuntu)
X-Powered-By: PHP/5.5.9-1ubuntu4.21
Connection: close
Content-Type: text/html

root@e514b399d69d:~# puppet apply 0-strace_is_your_friend.pp
Notice: Compiled catalog for e514b399d69d.ec2.internal in environment production in 0.02 seconds
Notice: /Stage[main]/Main/Exec[fix-wordpress]/returns: executed successfully
Notice: Finished catalog run in 0.08 seconds
root@e514b399d69d:~# curl -sI 127.0.0.1:80
root@e514b399d69d:~#
HTTP/1.1 200 OK
Date: Fri, 24 Mar 2017 07:11:52 GMT
Server: Apache/2.4.7 (Ubuntu)
X-Powered-By: PHP/5.5.9-1ubuntu4.21
Link: <http://127.0.0.1/?rest_route=/>; rel="https://api.w.org/"
Content-Type: text/html; charset=UTF-8

root@e514b399d69d:~# curl -s 127.0.0.1:80 | grep Holberton
<title>Holberton &#8211; Just another WordPress site</title>
<link rel="alternate" type="application/rss+xml" title="Holberton &raquo; Feed" href="http://127.0.0.1/?feed=rss2" />
<link rel="alternate" type="application/rss+xml" title="Holberton &raquo; Comments Feed" href="http://127.0.0.1/?feed=comments-rss2" />
<div id="wp-custom-header" class="wp-custom-header"><img src="http://127.0.0.1/wp-content/themes/twentyseventeen/assets/images/header.jpg" width="2000" height="1200" alt="Holberton" /></div>
<h1 class="site-title"><a href="http://127.0.0.1/" rel="home">Holberton</a></h1>
<p>Yet another bug by a Holberton student</p>
```

## Repository
- **GitHub Repository**: `alx-system_engineering-devops`
- **Directory**: `0x17-web_stack_debugging_3`
- **File**: `0-strace_is_your_friend.pp`

---

© 2024 ALX, All rights reserved.