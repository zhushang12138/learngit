Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
mi@lenovo MINGW64 ~/Desktop
$ git config --global user.name "zhushang"

mi@lenovo MINGW64 ~/Desktop
$ git config --global user.email "365584079@qq.com"

mi@lenovo MINGW64 ~/Desktop
$ mkdir learngit

mi@lenovo MINGW64 ~/Desktop
$ cd learngit
p
mi@lenovo MINGW64 ~/Desktop/learngit
$ pwd
/c/Users/mi/Desktop/learngit

mi@lenovo MINGW64 ~/Desktop/learngit
$ git init
Initialized empty Git repository in C:/Users/mi/Desktop/learngit/.git/

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add readme.txt
fatal: pathspec 'readme.txt' did not match any files

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git commit -m "wrote a file named readme"
[master (root-commit) fb9a807] wrote a file named readme
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ ^C

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ ^C

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git diff
diff --git a/readme.txt b/readme.txt
index d8036c1..013b5bc 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1,2 +1,2 @@
-Git is a version control system.
+Git is a distributed version control system.
 Git is free software.
\ No newline at end of file

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt


mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git commit -m "add distribute"
[master f0b66e3] add distribute
 1 file changed, 1 insertion(+), 1 deletion(-)

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
nothing to commit, working tree clean

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git commit -m "append GPL"
[master 4d09107] append GPL
 1 file changed, 1 insertion(+), 1 deletion(-)

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log
commit 4d091079803fa5f41e2e312197198b7f430eb4c7
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:55:41 2018 +0800

    append GPL

commit f0b66e3b22deb8f23f84d6cf4749faa8703abb61
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:49:18 2018 +0800

    add distribute

commit fb9a8075885621136b57abed7668698ec5aa5db6
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:33:35 2018 +0800

    wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log --pretty=oneline
4d091079803fa5f41e2e312197198b7f430eb4c7 append GPL
f0b66e3b22deb8f23f84d6cf4749faa8703abb61 add distribute
fb9a8075885621136b57abed7668698ec5aa5db6 wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reset --hard HEAD^
HEAD is now at f0b66e3 add distribute

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log
commit f0b66e3b22deb8f23f84d6cf4749faa8703abb61
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:49:18 2018 +0800

    add distribute

commit fb9a8075885621136b57abed7668698ec5aa5db6
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:33:35 2018 +0800

    wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reset --hard 4d0910
HEAD is now at 4d09107 append GPL

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reflog
4d09107 HEAD@{0}: reset: moving to 4d0910
f0b66e3 HEAD@{1}: reset: moving to HEAD^
4d09107 HEAD@{2}: commit: append GPL
f0b66e3 HEAD@{3}: commit: add distribute
fb9a807 HEAD@{4}: commit (initial): wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        LICENSE.txt

no changes added to commit (use "git add" and/or "git commit -a")

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add LICENSE.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   LICENSE.txt
        modified:   readme.txt


mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git commit -m "understand how stage works"
[master 9860644] understand how stage works
 2 files changed, 4 insertions(+), 1 deletion(-)
 create mode 100644 LICENSE.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ Git tracks changes.
git: 'tracks' is not a git command. See 'git --help'.

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git checkout -- readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt


mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
shit
mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reset HEAD readme.txt
Unstaged changes after reset:
M       readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git checkout -- readme.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
nothing to commit, working tree clean

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        test.txt

nothing added to commit but untracked files present (use "git add" to track)

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git commit test.txt -m "add test.txt"
[master cbf0e1b] add test.txt
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ rm test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        deleted:    test.txt

no changes added to commit (use "git add" and/or "git commit -a")

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git checkout -- test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        deleted:    test.txt

no changes added to commit (use "git add" and/or "git commit -a")

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git rm test.txt
rm 'test.txt'

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        deleted:    test.txt


mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git commit -m "remove test.txt"
[master 4a7ef93] remove test.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
nothing to commit, working tree clean

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log
commit 4a7ef93332742a91d299924c411dc299cb964968
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 20:22:07 2018 +0800

    remove test.txt

commit cbf0e1b7600487fc93f8c0957e4dc2bff30a34d8
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 20:15:55 2018 +0800

    add test.txt

commit 98606440b69591baf83e8a34b383f101c285f67a
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 19:41:17 2018 +0800

    understand how stage works

commit 4d091079803fa5f41e2e312197198b7f430eb4c7
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:55:41 2018 +0800

    append GPL

commit f0b66e3b22deb8f23f84d6cf4749faa8703abb61
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:49:18 2018 +0800

    add distribute

commit fb9a8075885621136b57abed7668698ec5aa5db6
Author: zhushang <365584079@qq.com>
Date:   Wed Jun 13 16:33:35 2018 +0800

    wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log pretty=online
fatal: ambiguous argument 'pretty=online': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log --pretty=online
fatal: invalid --pretty format: online

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log -- pretty=online

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git log -- pretty=oneline

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reflog
4a7ef93 HEAD@{0}: commit: remove test.txt
cbf0e1b HEAD@{1}: commit: add test.txt
9860644 HEAD@{2}: commit: understand how stage works
4d09107 HEAD@{3}: reset: moving to 4d0910
f0b66e3 HEAD@{4}: reset: moving to HEAD^
4d09107 HEAD@{5}: commit: append GPL
f0b66e3 HEAD@{6}: commit: add distribute
fb9a807 HEAD@{7}: commit (initial): wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git checkout -- test.txt
error: pathspec 'test.txt' did not match any file(s) known to git.

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reset --hard cbf0e
HEAD is now at cbf0e1b add test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git check -- test.txt
git: 'check' is not a git command. See 'git --help'.

Did you mean one of these?
        checkout
        check-attr
        cherry

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git checkout -- test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git status
On branch master
nothing to commit, working tree clean

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reset --hard 4d0910
HEAD is now at 4d09107 append GPL

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reflog
4d09107 HEAD@{0}: reset: moving to 4d0910
cbf0e1b HEAD@{1}: reset: moving to cbf0e
4a7ef93 HEAD@{2}: commit: remove test.txt
cbf0e1b HEAD@{3}: commit: add test.txt
9860644 HEAD@{4}: commit: understand how stage works
4d09107 HEAD@{5}: reset: moving to 4d0910
f0b66e3 HEAD@{6}: reset: moving to HEAD^
4d09107 HEAD@{7}: commit: append GPL
f0b66e3 HEAD@{8}: commit: add distribute
fb9a807 HEAD@{9}: commit (initial): wrote a file named readme

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git add test.txt
fatal: pathspec 'test.txt' did not match any files

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git reset --hard 4a7e
HEAD is now at 4a7ef93 remove test.txt

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$ git checkout -- test.txt
error: pathspec 'test.txt' did not match any file(s) known to git.

mi@lenovo MINGW64 ~/Desktop/learngit (master)
$





master--------（切换到master分支，创建bug分支。对于bug分支的修改进行合并。删除bug分支转到dev分支）
              --------bug（转到bug分支，对master已经提交过的修改进行修改，然后提交，转到master分支）
			  
dev-----------（啥也没干，工作区文件LICENSE.txt已经修改，保存到stash中。读取stash中的内容）
