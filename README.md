
#使用与配置Hexo
##2016.04.15
###添加RSS和sitemap
####通过npm安装插件
```
npm install hexo-generator-feed@1.0.3 --save
npm install hexo-generator-sitemap@1.0.1 --save
```
####修改全局配置文件_config.yml
```
#添加如下配置
feed:
  type: atom ##feed类型 atom或者rss2
  path: atom.xml ##feed路径
  limit: 20  ##feed文章最小数量
```
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
