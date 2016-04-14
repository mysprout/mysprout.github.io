#记录每日发表的文章
##2016.04.13
- WordPress-Plugins-WordPress使用笔记 — 插件篇（SyntaxHighlighter）
- Android-Notes-在Button控件上显示倒计时
- Android-Notes-为TextView、Button控件上的文本添加图标
- Android-Notes-清单合并

##2016.04.12
- Android-Study-Android学习之路(1) -- APK签名

#使用与配置Hexo
##2016.04.14
###将我的博客同时托管到github和coding
将博客同时托管在国外和国内，通过DNSPOD分流，在国内访问coding，国外访问github，在执行时，出现了些问题，记录下来。

- 我是现将hexo托管到github的，那么在coding托管的时候，项目名就必须和github的用户名相同，不然部署到git后，github上显示正常，coding上就不会显示样式
- 执行hexo d上传到git时，因为我同时上传到两个平台，在修改_config.yml的deploy时，我使用回车换行，写不同的平台，执行hexo d命令时，会报格式不正确。

```
#这里是正确的格式
deploy:
  type: git
  message: ""
  repo: 
    github: https://github.com/mysprout/mysprout.github.io.git,master
    coding: https://git.coding.net/mysprout/mysprout.git,coding-pages
```
