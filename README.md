# markdown_elegantly
 How to write markdown elegantly. Continuously updating...

## 如何用VSCode写markdown

#### 关于预览

软件自带预览功能，普通的预览功能不需要安装插件，只需在所编辑文档右上角点击‘open preview to the side’，即可实现编辑和预览同时进行。

![20221228111930](https://cdn.jsdelivr.net/gh/fathug/PicBed@main/picgo/20221228111930.png)

#### 关于如何快捷贴入图片，并上传至图床

笔者觉得将图片放在本地，无法实现供其他读者浏览的目的，故基本都是将开源内容中的图片上传至网络图床，供网友浏览。

笔者使用的编辑软件为VSCode，使用的插件为PicGo，图床为Github。其中配置方法可以参考[ref](https://blog.csdn.net/qq_44314954/article/details/122951033)。

快捷上传图片的方法是ctrl+alt+u。（图片贴入文本中，也会同时上传至Github图床）

#### 关于其他易于使用的插件

1. Markdown Editor
   可实现即时渲染的功能，所见即所得，和Typora类似。但是插件还有需要优化的地方，笔者用的时候发现光标的定位不准。  
   ref：https://marketplace.visualstudio.com/items?itemName=zaaack.markdown-editor  
   ref：https://www.v2ex.com/t/769051
2. Markdown Preview Enhanced
   弥补自带预览功能的不足
3. Markdown All in One  
   提供自动补全功能和快捷键功能

## 如何用Typora写markdown

Typora是实时渲染的编辑器，目前是收费使用，自行安装即可。

#### 关于如何快捷贴入图片，并上传至图床

所需软件：PicGo

步骤：

1. 在Github中新建一个仓库，作为图床存放图片

   仓库设置为public（*这很重要，若设置为private，则图片无法在编辑器中显示*）

2. 获取Tokens

   在Github网页端依次点击：头像、Settings、Developer settings、Tokens、Genenrate new token（此处需要填写token相关信息，其中Note随便写、Expiration设为No expiration，scopes的选项全部勾选，然后Generate即可）

   （*token只能看到一次，请备份留作备用*）

3. 安装并配置PicGo

   进入PicGo，在图床设置中选择Github，以下是所需填写的内容：

   > - 仓库名：用户名/仓库，例如`username/reponame`
   > - 分支名：通常写`main`
   > - Token：填入2.中的token即可
   > - 存储路径：例如`img/` ，这是仓库内的相对路径，上传后的图片会进入到这个路径内；若没有该路径，图片上传后会自动创建该路径
   > - 自定义域名：通常使用`https://raw.githubusercontent.com/用户名/仓库名/main` ，若在使用过程中图片加载过慢，可以考虑更换为`https://cdn.jsdelivr.net/gh/用户名/仓库名@main`实现加速

   设为默认图床即可

4. 配置Typora

   进入设置，设置如下：

   > 插入图片时：选择上传图片、勾选对本地位置的图片应用和对网络位置的图片应用（若不勾选，网络图片的图床失效后，图片就无法显示）
   >
   > 上传服务设定：选择PicGo(app)、路径选择PicGo.exe的路径，例如`C:\Program Files\PicGo\PicGo.exe`
   >
   > 点击*验证图片上传选项*

   
