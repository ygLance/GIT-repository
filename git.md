# git使用笔记
*****
 ## 本地创建仓库

```
git init
```
* 在目录中创建新仓库
* 此时在目录下创建一个隐藏的.git子目录
*******
## 基本配置
```
git config -global core.editer vim
```
* 默认编辑器
******
## 基本操作
```
git add
```
* 将该文件添加到缓存
* 用.通配所有文件
```
git status -s
```
* 查看简略信息
* A:已添加到缓存
* AM:添加到缓存后有变动 需要再次 add
*****
## clone一个仓库
```
git clone [url]
如:git clone git@github.com:name/repository.git

```
* clone完会生成simplegit子目录
* git默认使用url指向项目的名字作为本地仓库名
* 可以在clone命令后加想要的名字