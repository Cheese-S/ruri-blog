#成为自主搭建blog的技术猛女指南

```test``` <- 代表在终端输入 

## 需要安装的
- homebrew
  - 一个包管理器
  - ```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```
    - 等字跳完后输入```brew --version```来检查是否下载成功
- git
  - 大名鼎鼎的git
    - 管理版本的
      - 想象一条河有不同的干道,git就是帮你管理分叉然后再合并的
  - ```brew install git```
- nodejs
  - 我们搭建网站需要的杂七杂八的东西都在里面
  - ```brew install npm```
    - 用以下指令来检查是否下载成功
      - ```node -v```
      - ```npm -v```
- yarn
  - 网页的包管理器
  - ```npm install --global yarn```
    - 检查
      - ```yarn --version```
- hexo
  - 我们(你)的博客框架!
  - ```yarn add -g hexo```
    - 检查
      - ```yarn run hexo -v```

- vscode
  - 写您的文章用的 相当于wps
  - https://code.visualstudio.com/download

## 下载您的博客
- ```git clone https://github.com/Cheese-S/ruri-blog.git```
  - 这个会在你终端的当前文件夹内下载一个叫做**ruri_blog**的文件夹
    - 例子![](img/2023-09-30-22-41-25.png) 
  - 用 **vscode** 打开这个文件夹
  - ```yarn install```

## 写博客
- ```yarn run hexo serve```
  - 如果你想看到草稿的话
    - ```yarn run hexo serve --drafts```
  - http://localhost:4000/ 浏览器打开这个网址
    - 恭喜你!!在本地部署了你的博客!
  - 打开 source/_posts/hello-world.md
    - 修改并保存，你的浏览器应该会自动刷新
    - 你可以实时看到自己blog修改之后的样子！
- ```yarn run hexo new draft "name"```
  - 创造一个新的草稿
    - 正式部署在网络上是看不见的
  - 把name改成你想要的标题
    - 例如标题是 我爱吃西瓜
      - ```yarn run hexo new draft "我爱吃西瓜"```
- ```yarn run hexo publish draft "name"```
  - 发表一个草稿 
    - 正式部署的时候就看见了
- ```yarn run hexo new post "name"```
  - 创立一个新的文章 **注意：不是草稿**
