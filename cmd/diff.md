git diff
==========

和linux下的diff一样,不用文件参数,直接比较最后一次commit和当前的不同.

其实也不是最后一次commit,是放在.git的中间态.用这个命令常用于提交前看修改了哪些地方.

可以看出diff出来的格式和linux下自带的diff -u file1 file2是一样的.

也和svn diff出来的效果是一样的.因此也是可以用git diff做一个patch的.

patch中文是补丁,linux内核打补丁通常就用这个命令.

    git diff > myupdate.patch

打补丁就是patch -p0 < myupdate.patch

不过要注意的是git diff是无视新增的文件的,他只管修改的文件





