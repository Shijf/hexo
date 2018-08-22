---
title: build-a-fast-and-elegant-laravel-development-environment
categories:
  - others
  - Laravel
  - PHP
tags:
  - php
  - laravel
date: 2018-08-22 15:16:19
---

首先感谢 Summer 的这几本 laravel [教程](https://laravel-china.org/courses) ，一直也跟着教程一点点的学过来的 ，真的讲得很仔细，学习了不少知识，在此真心的感谢他。在学习初期，最烦恼的就是环境的搭建，记得第一次跟着教程走的时候，因为我的电脑用户名不是英文的，真的是搞了好久。打算写这篇文章的时候，是昨天刚刚重装了系统，可是再安装 homestead 的时候，还是遇到这样那样的问题，虽然都解决了，但是假如我是一个初学者的话，想想都头疼，所以就想写一篇文章，实际还是可以用其他环境的，让学习的门槛低一点，也算是一个配置的备忘录吧！
搭建 PHP 开发环境 从初学到现在用了很多的开发环境 别的就不说了 这边推荐 两种 一个是 laravel 官方推荐的 homestead 还有比较火的 laragon ，前者的介绍就直接阅读 laravel 的官方文档就可以了，后者的介绍看下[laragon 中文网](http://www.laragon.com.cn/) 。

安利一下 laragon ，此工具 包含了 Apache、MySQL、MariaDB、PHP、Nodejs、npm、phpMyAdmin、git、ssh、cmder、Memcached、Redis、composer、Debug,2.0新增Sublime Text、ngrok、7z等工具，尤其是 ngrok ，在我开发微信应用的时候，帮了很大的忙，之前是买的，现在直接用这个就可以，也算是省了一笔费用，还是很稳定的，基本很长时间不会掉线。

今天在用hosestead 开发环境，在使用 yarn 安装前断流的时候们总是出错，虽然我之前也遇到过类似的问题，可是都是按[这种方法](https://laravel-china.org/topics/3570/yarn-install-error-learning-laravel-entry-manual-encounter-problems-to-help#reply35724)解决了，可是感觉 win 下开发，这些方法真的是可遇不可求呀，今天就怎么都解决不了这些问题，于是乎偶然在论坛看到了[这个](https://laravel-china.org/articles/5083/on-the-record-of-installing-the-node-sass-error)解决方法，试了以后 表现非常好（这个是在 laragon 环境中用的），再次也表示感谢，作者也写了好多的应对措施。好了下面是搭建一个在 win 下开发 laravel（其实其他框架也是可以用的）的，也是非常方便的，速度很快！ 

1. 安装 [laragon](https://sourceforge.net/projects/laragon/files/releases/3.1/laragon-wamp.exe/download) ，一直下一步就可以，安装位置随便定。
2. 使用的话就是大家，看下官网就可以了。
3. 如果要使用前端流的话，就可以参考[这个](https://laravel-china.org/articles/5083/on-the-record-of-installing-the-node-sass-error)，安装下 yarn 。
4. 其实就可以愉快的用了。


实际主要是想说，在配置前端流的时候的一些配置，就可以很快的进行开发了，这里就先搬过来[这个](https://laravel-china.org/articles/5083/on-the-record-of-installing-the-node-sass-error)，
1. 将 npm 源切换至淘宝源
`npm config set registry https://registry.npm.taobao.org`
2. 通过 npm 全局安装 yarn
`npm install -g yarn`
3. 安装 cross-env 
`npm i -g cross-env`
4. 将 yarn 源切换至淘宝源
`yarn config set registry https://registry.npm.taobao.org`
5. 执行 yarn install 

`yarn install` （如果是遇到 error An unexpected error occurred: "EINVAL: invalid argument, symlink） 请运行 `yarn install --no-bin-links`  ，不过我没有遇到这个错误。
6. 执行  npm run dev 或者 npm run watch-poll 还有不必改 ` package.json` 这个文件
 ` npm run dev`  或者  ` npm run dev `
 
7. 执行完这几个步骤，就可以愉快的练习这个教程了，不然前端编译不通过，还真的是很苦恼的，这也算是一个记录吧，最后来几张图吧~


![file](https://lccdn.phphub.org/uploads/images/201805/31/18751/YKuSiPG2RT.png?imageView2/2/w/1240/h/0)
ngrok 这个挺好用的
![file](https://lccdn.phphub.org/uploads/images/201805/31/18751/L1dTcgQScK.png?imageView2/2/w/1240/h/0)


