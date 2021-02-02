---
title: myblog
date: 2021-02-02 14:43:42
top: 5
---

# 基于hexo框架，搭建个人博客
<!-- more-->

## 基本操作步骤:
### (一). 本地安装node.js 6.x版本以上(这里默认已安装[nodejs官方下载链接](https://nodejs.org/zh-cn/download/))。
### (二). 本地安装git [git下载链接](https://git-scm.com/downloads)。
### (三). 开始安装hexo:


1. 安装cnpm，国内淘宝镜像
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
卸载：
```
sudo npm uninstall cnpm -g
```

2. 安装hexo
```
sudo cnpm install hexo-cli -g
```
卸载：
```
sudo cnpm uninstall hexo-cli -g
```

3. 初始化hexo项目
```
sudo hexo init
```

4. 构建hexo项目
```
sudo hexo generate
```

5. 启动hexo服务
```
sudo hexo server
```

6. 清理hexo构建项目
```
sudo hexo clean
```

### (四). 更换设置主题
1. 下载yilia主题
```
git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia
```

2. 配置根目录下_config.yml
```
theme: yilia
```

3. 为了显示全目录，项目根目录下安装jsoncontent插件
```
sudo cnpm i hexo-generator-json-content --save
```

4. 配置项目根目录下的_config.yml
```
jsonContent:
  meta: false
  pages: false
  posts:
    title: true
    date: true
    path: true
    text: false
    raw: false
    content: false
    slug: false
    updated: false
    comments: false
    link: false
    permalink: false
    excerpt: false
    categories: false
    tags: true
```

### (五). 部署到github上
1. 安装deploy插件
```
sudo cnpm install hexo-deployer-git --save
```

2. github上新建仓库，名称必须是
```
github账户名.github.io
```

3. 配置根目录下的_config.yml
```
deploy:
  type: git
  repo: https://github.com/github账户名/github账户名.github.io
  branch: master
```

4. 发布
```
sudo hexo deploy
```

---
---
## 该个人博客项目已配置好上述操作，克隆下来以后调试步骤:
1. 切换到项目根目录
```
cd blog
```

2. 安装package记录的相关插件
```
sudo cnpm install --save
```

---
#### 调试过程中缺少相应插件，根据上述基本操作步骤，安装即可。
