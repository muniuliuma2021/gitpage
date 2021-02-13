---
title: 使用hexo和github搭建博客
date: 2021-2-12 13:32:53
tags:
- Skill
---

#### 1.环境准备：

​    安装git和nodejs
​    安装hexo: 

``` bash
$npm install -g hexo-cli
```



#### 2.初始化gitpage

``` bash
​$hexo init <folder>   #e.g: hexo init gitpage
​$cd <folder>          #e.g: cd gitpage
​$npm install
```

#### 3.本地测试是否成功

``` bash
​$hexo clean
​$hexo g # 生成
​$hexo s #hexo s是开启本地预览服务，打开浏览器访问 http://localhost:4000
``` 
执行以上命令之后，hexo就会在public文件夹生成相关html文件，这些文件将来都是要提交到github去的;

#### 4.配置_config.yml中有关deploy的部分：

``` bash
$npm install hexo-deployer-git --save
``` 
配置/_config.yml中有关deploy的部分(注意格式，很重要，不然无法部署):
```c
deploy:
  type: git
  repo: git@github.com:muniuliuma2021/muniuliuma2021.github.io.git
  branch: master
```

#### 5.部署并在github备份源码

``` bash
​hexo deploy  #部署到muniuliuma2021.github.io
​gitpush           #push 到GitHub备份
``` 

#### 6.修改主题

​在https://hexo.io/themes 下载喜欢的主题，我选的是cactus
``` bash
​$cd gitpage
​$git clone https://github.com/probberechts/hexo-theme-cactus.git themes/cactus
```
​修改/_cibfug.yml文件
​   -theme: landscape
​   +theme: cactus

#### 7.上传github备份

#### 8.修改头像等

#### 9.github备份

#### 10.添加/修改个人信息

#### 11.github备份

#### 12.添加tag：Deployment_complete
``` bash
git tag -a Deployment_complete
git push Deployment_complete origin
``` 