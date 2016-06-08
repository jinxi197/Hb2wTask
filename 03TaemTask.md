03组 飞车组

队长：CapJack
刘阳
喵喵
王晟-Eric

一、工作区、暂存区和版本库的理解

工作区：我们初始化的一个文件夹作为git的仓库，这个文件夹就是git的工作区。

暂存区：英文叫stage,或index。在版本库.git）目录下，有一个index文件（二进制文件）。它实际上就是一个包含文件索引的目录树，像是一个虚拟的工作区。在这个虚拟工作区的目录树中，记录了文件名、文件的状态信息（时间戳、文件长度等），文件的内容并不存储其中，而是保存在Git对象库（.git/objects）中，文件索引建立了文件和对象库中对象实体之间的对应。如果当前仓库，有文件更新，并且使用git add命令，那么这些更新就会出现在暂存区中。

版本库：当前仓库下，如果没有任何的提交，那么版本库就是对应上次提交后的内容。下面这个图展示了工作区、版本库中的暂存区和版本库之间的关系。

![](http://upload-images.jianshu.io/upload_images/1804917-84c7db5bd62badfe.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

二、github上我们之前做过什么

在github上我们做过的操作：

1、add sshkey

2、new repository（仓库）

github上的repository，我认为是一个最终的版本库，因为我们最终都是要推送到repository中的，其它的操作基本上都是在本机上。

三、举例说明工作区、暂存区、版本库与github上的repository的关系

![](http://upload-images.jianshu.io/upload_images/1804917-535d1a9ecc5526b9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

举个例子来说明吧：背景，一个班30人要交作业，班上分为3个小组，有一个学习委员。

工作区 —— 班上的同学作业

暂存区 —— 每个组的同学的作业都已经交给组长了

版本库 —— 每个组的组长已经把作业交给学习委员了

Github中的repository—— 学习委员交给老师了

以上就是我对这四者之间的关系的理解。

四、通过github的操作说明工作区、暂存区和版本库

![](http://upload-images.jianshu.io/upload_images/1804917-12e38f7504b77758.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

上图很清晰的给我们介绍了github与本机的一些常用到的操作。fork我们在这次作业的提交中也学习到了。在这次提交作业过程中，我们有一个前提和三个步骤，如下：

前提：组员fork组长的 Github 中 “ Hb2wTask ” 项目，fork之后，我们自己的github仓库中就会出现“ Hb2wTask ” 项目。

步骤一：在自己的 Github 中打开 “ Hb2wTask ” 项目，点开你的小组对应的文档后，点击 ✎ ,即可在远程库编辑文件了 —— 小组对应的文档 可以看做是本机的工作区

步骤二：编辑完成后，在网页底部添加本次修改备注及描述（描述可以不填），点击 Commit chenga ,完成提交 —— 点击 Commit chenga 相当于我们在本机中使用命令 add ，然后就到缓存区了。我们的项目主页，在 Code 中就可以看到我们修改过的文档了，没有pull requests的文档都可以看到

步骤三：推送 Pull requests，那么我们修改之后的项目就可以被推送到组长的项目中了 —— 本机中的push
以上就是我对工作区、暂存区和版本库通过github上的操作的理解。
