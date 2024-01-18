---
title: Ubuntu Setup!
date: 2024-01-10 12:00:00 0530
categories: [snippets, setup]
tags: [ubuntu,setup]
---

For ease, create bash script and execute it in one go.

```
# Install common libs
apt-get update && apt-get install -y git openssh-server libmagic-dev zsh libyaml-dev tinyproxy git-secret

# Install Node
curl -fsSL https://xdeb.nodesource.com/setup_lts.x | sudo -E bash -
apt-get install -y nodejs
npm install --global yarn

# Install Python 
sudo apt-get install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev openssl libffi-dev libsqlite3-dev
wget https://www.python.org/ftp/python/3.7.13/Python-3.7.13.tgz
tar xzvf Python-3.7.13.tgz
cd Python-3.7.13
./configure --enable-optimizations
make altinstall
ln -s /usr/local/bin/python3.7 /usr/bin/python3

# git change editor
git config --global core.editor "vim"
```