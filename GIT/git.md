# git使用笔记
*****
 ## 本地创建仓库

```
git init
```
* 把此目录变成git仓库
* 此时在目录下创建一个隐藏的.git子目录
*******
## 基本配置
```
git config -global core.editer vim
```
* 默认编辑器
******
## 基本文件操作
```
git add
```
* 将该文件添加到缓存
* 用.通配所有文件
```
git commit -m " ..."
```
* 提交修改
* 写备注
```
git status -s
```
* 查看简略信息
* A:已添加到缓存
* AM:添加到缓存后有变动 需要再次 add

```
git remote add origin [url]
git push -u origin master
```
* 仓库关联
* 第一次连接 提交
*****
```
git push
```
* 第二次以后的push

**文件夹?**
直接添加就行,但是文件夹不能是空的
******

## 版本回退
```
git reset -hard HEAD^
git reset -hard HEAD^^
git reset -hard HEAD~100
```
* 回退一个
* 两个
* 多个
******
* 第二次以后的提交
```
git log
```
* 查看log
## clone一个仓库
```
git clone [url]
如:git clone git@github.com:name/repository.git
```
* clone完会生成simplegit子目录
* git默认使用url指向项目的名字作为本地仓库名
* 可以在clone命令后加想要的名字
********
## 报错
```
The authenticity of host 'github.com (192.30.255.112)' can't be established.
```
* 链接github的repository时
* 缺少一个配置文件 ,输入yes 回车自动生成即可
* 缺的是.ssh下的kown_hosts
```
! [rejected] master -> master (fetch first)error:....
```
* push时
* 手动在github的web端做了编辑
* git pull 同步
* 然后git push再推
