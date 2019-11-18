---
title: 使用hexo加gitpage搭建自己的博客
date: 2019-11-18 10:52:20
tags: 博客系统搭建
---
### hexo安装
- hexo需要git'和node的支持，在之前请安装好这两个环境
- 安装的步骤，[官方网址]( https://hexo.io/zh-cn/ )
  - npm安装
    
    `hexo
    npm install hexo-cli -g`
    
  - 初始化一个网站(blog是文件夹的名字)
    
    ` hexo init blog `
    
  - 安装一些未安装好的插件
  
    ```
    cd blog
    npm install
    ```
  
  - 启动hexo服务
  
    `hexo server(s)`

### 部署到gitpages

- 使用travis-ci自动部署方式

  - 步骤：[官方网址](https://hexo.io/zh-cn/docs/github-pages)

  - 整体思路：travis-ci与github配合实现自动部署，travis-ci会把master分支进行构建（配置文件配配置的）构建到gh-pages分支上

  - 遇到问题

    - edge: true

      必须在配置文件的deploy:加上这个配置不然要报丢掉token异常

- 使用 [hexo-deployer-git](https://github.com/hexojs/hexo-deployer-git) 插件手动部署
  - 步骤：[官方网址]( https://hexo.io/zh-cn/docs/one-command-deployment )
  - 整体思路：使用插件提交到对应分支

