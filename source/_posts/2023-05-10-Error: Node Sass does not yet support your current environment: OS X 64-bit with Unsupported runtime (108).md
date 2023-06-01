---
title: "Error: Node Sass does not yet support your current environment: OS X 64-bit with Unsupported runtime (108)"
date: 2023-05-10 19:37:09
tags: [小bug真要命]
---
由于项目中使用的**node**版本是**18.16.0**，**node-sass**的版本是**4.7.2**，两者版本不兼容，导致此问题的出现。
## 解决办法
使用[n – Interactively Manage Your Node.js Versions](https://www.npmjs.com/package/n)来切换**node**的版本，可在[node-sass](https://github.com/sass/node-sass)快速指南中找到可使用**node**版本
```bash
npm install -g n
n 14
# 如果其中一个命令没有通过，您可能需要使用 sudo
sudo npm install -g n
sudo n 14
```


