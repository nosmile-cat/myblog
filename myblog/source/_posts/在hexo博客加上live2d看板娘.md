@[TOC](在hexo博客加上live2d看板娘)

## 1.首先安装[npm](https://nodejs.org/en/)包
- 配置环境变量
- 打开cmd.exe,输入:
```cmd
//查看版本号是否安装成功
$ npm -v
```
## 2.  下载hexo
- 输入命令
 ```cmd
//下载hexo客户端
$ npm install -g hexo-cli
```
- 同样环境变量
## 3.在本地新建文件==myblog==(作为博客资源文件夹)
- 输入命令
 ```cmd
//初始化刚新建的myblog文件夹
$ hexo init myblog
$ cd myblog
$ hexo instal
```
- 这时myblog就会生成以下文件![在这里插入图片描述](https://img-blog.csdnimg.cn/20190926141412997.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM0Njc0MDI=,size_16,color_FFFFFF,t_70)
## 4.第一个博客出来了，我们试试运行
- 输入命令
 ```cmd
//启动命令(完整命令:hexo server)
$ hexo s
```
我们可以看到下面生成的url
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190926142135894.png)
在浏览器上预览
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190926142303454.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM0Njc0MDI=,size_16,color_FFFFFF,t_70)
## 5.下面进入重点加上看板娘，详细[文档](https://github.com/EYHN/hexo-helper-live2d/blob/master/README.zh-CN.md)
- 回到当前窗口myblog路径输入命令：
 ```cmd
//下载live2d包
$ npm install --save hexo-helper-live2d
```
- 再下载模型
 ```cmd
//下载模型
$ npm install live2d-widget-model-hibiki
```
##### #更多模型选择
- live2d-widget-model-chitose
- live2d-widget-model-epsilon2_1
- live2d-widget-model-gf
- live2d-widget-model-haru/01 (use npm install --save live2d-widget-model-haru)
- live2d-widget-model-haru/02 (use npm install --save live2d-widget-model-haru)
- live2d-widget-model-haruto
- live2d-widget-model-hibiki
- live2d-widget-model-hijiki
- live2d-widget-model-izumi
- live2d-widget-model-koharu
- live2d-widget-model-miku
- live2d-widget-model-ni-j
- live2d-widget-model-nico
- live2d-widget-model-nietzsche
- live2d-widget-model-nipsilon
- live2d-widget-model-nito
- live2d-widget-model-shizuku
- live2d-widget-model-tororo
- live2d-widget-model-tsumiki
- live2d-widget-model-unitychan
- live2d-widget-model-wanko
- live2d-widget-model-z16
### ....
## 6.下载完模型后在根目录的 node_modules 文件夹下找到刚才下载的live2d-widget-model-hibiki模型，将其复制到新建目录 live2d_models 下
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190926144043742.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM0Njc0MDI=,size_16,color_FFFFFF,t_70)

## 7.在根目录_config.yml配置下添加以下参数，唯一改变是参数==model.use== 是下载模型名称
 ```yaml
#参数配置
live2d:
  enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  debug: false
  model:
    use: live2d-widget-model-hibiki   #下载模型参数
  display:
    position: right
    width: 150
    height: 300
  mobile:
    show: true
```

## 最后再次运行$hexo s，看效果，右下角萌萌哒看板娘出来了
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190926144418709.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM0Njc0MDI=,size_16,color_FFFFFF,t_70)
###### #第一次写博客，参考文章[1](https://www.jianshu.com/p/4b61d8702cfa)

