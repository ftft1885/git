Lesson-1
========
使用git，特指github。最开始只需要会3个git命令

+ git add [file]

+ git commit -m "sth"

+ git push

github的操作示例
------------
    touch README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin https://github.com/ftft1885/git.git
    git push -u origin master


非常完整的讲了建git的repo以及第一次提交

git中的一些基本概念
--------------
repo是repository的简称，中文是仓库的意思，repo是git的基本单元，git不像svn那样可以分路径，每次git clone必然是整个repo

git init:

git init会在当前目录下新建一个隐藏文件夹.git，里面包含了各种信息，git命令只有在.git存在下才会起作用。当然删了.git整个目录就变得干净啦。（这点完爆svn，svn每个目录下都有.svn这个文件夹,而且巨大无比,想清掉这些还要递归删除.svn）

git add:

基本用法: git add myfile

要注意的是git毕竟不是像金山快盘,dropbox这种网盘,不是往里面塞东西就能随时加到repo中去的.你必须要手动add.这很关键,因为并不是每个目录下的文件你都想放入repo,比如一些test log key这些file.

对于多个文件,完全可以使用git add file1 file2 file3来写.

git commit:

基本用法: git commit -m "fix some bug"

这个-m后面输入的东西就是你的提交信息,这是必须要的,你可以理解为你的提交必须有意义.不是随意提交的

要注意的是git commit和svn的commit很不同,svn的commit需要联网,而git由于本身就是服务器,可以向本地提交,如果要同步到云端,要使用git push,可以说svn commit 差不多就是git commit + git push 的合并

git push:

基本用法: git push origin master

可以尝试下直接输入git push

fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>

git非常人性化的说"没有配置push的目的"

并且给出了配置push目的的方法

也就是github中给的那样

git remote add origin https://github.com/ftft1885/git.git

那个origin是指后面的网址的名字

你完全可以取个阿猫阿狗

git remote add amao https://github.com/ftft1885/git.git

这也是完全可以的.

要注意的是后面的网址并不一定是https,只是github比较牛逼,支持https协议,一般的话都是git://xxxxx.com之类的,这时候往往还需要搞ssh-key,非常麻烦.

git push origin master

这个origin就是上面我们给repo网址取的名字,master指的是主干,就是git的主干与分支的概念,后面再详细解释,总之就是push到这个repo的主干上就是啦

如果你出了这个错误怎么办?

    error: src refspec master does not match any.
    error: failed to push some refs to 'https://github.com/ftft1885/git.git'

那你一定是没有add啊混蛋..你没有做任何修改push个p啊









