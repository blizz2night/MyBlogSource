---
title: test
date: 2017-08-10 13:39:24
tags: [hexo,git,node]
---
# Ubuntu安装Hexo

标签（空格分隔）： hexo git node

踩了个坑，不要使用apt-get装nodejs，使用hexo server时，会报local hexo not found错误，即使安装hexo-server也没有用，因为nodejs版本太低 0.10。。。
如果已经在0.10环境下安装hexo
可以通过nvm重装node
nvm安装方法在https://github.com/creationix/nvm#install-script
```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
```
安装nodejs
```bash
nvm install stable
```
装好后提示hexo、hexo-cli、hexo-server这仨可能继续依赖原始node
```bash
=> You currently have modules installed globally with `npm`. These will no
=> longer be linked to the active version of Node when you install a new node
=> with `nvm`; and they may (depending on how you construct your `$PATH`)
=> override the binaries of modules installed with `nvm`:

/usr/local/lib
├── hexo@3.3.8
├── hexo-cli@1.0.3
└── hexo-server@0.2.2
=> If you wish to uninstall them at a later point (or re-install them under your
=> `nvm` Nodes), you can remove them from the system Node as follows:

     $ nvm use system
     $ npm uninstall -g a_module
```
因此卸载
sudo npm remove -g hexo
sudo npm remove -g hexo-cli
sudo npm remove -g hexo-server

npm安装hexo 






