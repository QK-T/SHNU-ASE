# Git以及团队协作教程

@QK-T，moxiaozi

## 技术术语

1. **branch**

   A branch in Git is simply a lightweight movable pointer to a commit.

2. **checkout**
   To switch to an existing branch, we run the `git checkout` command.

3. **fetch**
   To synchronize our work with `remote/origin`, we run a `git fetch origin` command.

4. **HEAD**
   In Git, `HEAD` is a pointer to the local branch we're currently on.

5. **master**
   `Master` is the default branch name in Git.

6. **origin**
   `origin` is the default name for a remote when we run `git clone`.

7. **pull**
   `git pull` is essentially (`git fetch` + `git merge`).



## 图解Git命令及其工作过程

![](images/Git-1.png)

![](images/Git-2.png)

![](images/Git-3.png)

![](images/Git-4.png)

![](images/Git-5.png)

![](images/Git-6.png)

![](images/Git-7.png)

![](images/Git-8.png)

![](images/Git-9.png)



![](images/Git-10.png)

![](images/Git-11.png)

![](images/Git-12.png)

![](images/Git-13.png)

![](images/Git-14.png)

![](images/Git-15.png)

![](images/Git-16.png)

![](images/Git-17.png)

![](images/Git-18.png)

![](images/Git-19.png)

![](images/Git-20.png)

![](images/Git-21.png)







## GitHub以及团队协作

**Git-Flow 工作图示**

![](images/flow.png)

![](images/Git-flow.png)

以上分支的主要用途：

1. master分支，即主分支。任何项目都必须有个这个分支。对项目进行tag或发布版本等操作，都必须在该分支上进行。
2. develop分支，即开发分支，从master分支上检出。团队成员一般不会直接更改该分支，而是分别从该分支检出自己的feature分支，开发完成后将feature分支上的改动merge回develop分支。同时release分支由此分支检出。
3. release分支，即发布分支，从develop分支上检出。该分支用作发版前的测试，可进行简单的bug修复。如果bug修复比较复杂，可merge回develop分支后由其他分支进行bug修复。此分支测试完成后，需要同时merge到master和develop分支上。
4. feature分支，即功能分支，从develop分支上检出。团队成员中每个人都维护一个自己的feature分支，并进行开发工作，开发完成后将此分支merge回develop分支。此分支一般用来开发新功能或进行项目维护等。
5. fix分支，即补丁分支，由develop分支检出，用作bug修复，bug修复完成需merge回develop分支，并将其删除。所以该分支属于临时性分支。
6. hotfix分支，即热补丁分支。和fix分支的区别在于，该分支由master分支检出，进行线上版本的bug修复，修复完成后merge回master分支，并merge到develop分支上，merge完成后也可以将其删除，也属于临时性分支
