---
title: CentOS Setup!
date: 2024-01-10 12:00:00 0530
categories: [snippets, setup]
tags: [centos,setup]
---

For ease, create bash script and execute it in one go.

```
yum -y install epel-release 
yum -y update
yum groupinstall "Development Tools" -y
yum install libffi-devel zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gcc -y

# Python Installation
wget https://www.python.org/ftp/python/3.7.5/Python-3.7.5.tgz
# Alternatives: https://www.python.org/ftp/python/3.9.9/Python-3.9.9.tgz
tar -xzf Python-3.9.9.tgz
cd Python-3.7.12
./configure --enable-optimizations; make altinstall
```