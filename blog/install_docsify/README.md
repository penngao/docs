# 如何安装 docsify

## 环境需求

* Windows 10
* Scoop

## 安装

1. 在 Scoop 中通过 `npm init` 命令生成 package.json 文件，其中 `git repository: https://github.com/docsifyjs/docsify.git`。

2. 全局安装 docsify
   `npm i docsify-cli -g`

3. 新建 `docs` 文件夹

4. 初始化项目
   `docsify init ./docs`

5. 初始化成功后可以看到 ./docs 目录下创建的几个文件：
   index.html 入口文件
   README.md 做为主页内容渲染
   .nojekyll 用于阻止 GitHub Pages 会忽略掉下划线开头的文件
   直接编辑 docs/README.md 就能更新网站内容，也可以编写多个页面

6. 本地预览网站
   `docsify serve docs`

7. 安装 git
   `scoop install git`

8. 在 GitHub 新建名为 docs 的仓库

9. 在本地 ./docs 目录下进行 `git init`

10. 将本地仓库与远程仓库进行关联
    `git remote add origin git@github.com:yourname/docs.git`

11. 将 ./docs 目录的所有文件添加到暂存区
    `git add .`

12. 提交暂存区到仓库区
    `git commit -m [message]`

13. 将本地仓库内容推送到远程库上
    `git push -u origin master`

14. 在 GitHub 中 docs 仓库点击 Settings，找到 GitHub Pages 按如下方式进行设置

    <div align=GitHub Pages>
        <img width="300" src="../blog/install_docsify/assets/GitHub Pages.JPG">
    </div>

15. 在 https://yourname.github.io/docs/ 进行访问

## 参考

[有了 docsify 神奇，从此爱上看文档](https://www.jianshu.com/p/4883e95aa903)

[How to create a documentation site with Docsify and GitHub Pages](https://opensource.com/article/20/7/docsify-github-pages)

[廖雪峰 git](https://www.liaoxuefeng.com/wiki/896043488029600/898732864121440)

