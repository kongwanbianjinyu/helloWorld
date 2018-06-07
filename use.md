github使用方法
===

基本操作
---

打开git的bash，然后所有linux 的命令都可以在这里使用。

在bash里粘贴为Shift + Insert

1.首先明确工作目录，可根据需要cd进行切换

```bash
pwd
```

2.首先从网址克隆到本地，会自动在当前工作目录下建立一个项目文件夹

```bash
git clone https://github.com/kongwanbianjinyu/helloWorld.git
```

3.进入此项目文件夹

```bash
cd helloWorld
```

4.你可以在此目录下添加文件（文件放在与.git 文件夹同级目录下），或者更改已经存在的文件，然后再通过

```bash
git add hello.txt
git add 123.txt
```

将文件加入到文件管理系统，只有添加之后文件管理系统才会跟踪

5.当你更改完一个版本之后，想保存当前版本的状态，就可以对其进行提交

```bash
git commit -m "the second commit"
```

提交之后该版本就保留了下来，随时可以恢复

6.当最终版本做完，就可以发布到github 的网页上，供他人下载。

```bash
git push
```

------

技巧
---

### 查看文件状态

```bash
git status
```

该命令会显示目前项目中所有文件的状态，若还没有add到文件管理系统的，会用红色字体标明（或者是未跟踪，或者是已经修改），可以提交的会用绿色字体标出。对于标红的文件只需要执行下 add命令就可以了。

### 版本回退

```bash
git log
```

可以查看当前的提交版本信息，每次提交都有一个唯一的编号，会有作者和时间信息

```bash
commit 58377487ca2062c7275516fa8d2375fb692d941f (HEAD -> master, origin/master,                        origin/HEAD)
Author: kongwanbianjinyu <1146904763@qq.com>
Date:   Wed Jun 6 23:57:58 2018 +0800

    the third commit

commit 972b0df6a0400f8ec7fe69e73643ed143ee19b87
Author: kongwanbianjinyu <1146904763@qq.com>
Date:   Wed Jun 6 23:50:12 2018 +0800

    1

commit e80c749c7e428aa9c4872a69db439afd076f5235
Author: kongwanbianjinyu <39997683+kongwanbianjinyu@users.noreply.github.com>
Date:   Wed Jun 6 22:46:15 2018 +0800

    Initial commit
```

回退到58377（只需要输入一段，会自动匹配）版本：

```bash
git reset --hard 58377
```

这时候所有本地的改动都会被舍弃。

或者执行，默认回退到上一个版本：

```bash
git reset --hard HEAD^
```

### 多人合作

其他更新者更新代码之后，你可以直接用

```bash
git pull
```

在本地获取最新的代码。

我的本地代码也可以通过

```bash
git push 
```

推送到页面。

这样就可以了。

































