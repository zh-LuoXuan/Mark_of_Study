# git命令

#### 初始化git仓库

```bash
git init
```

#### 工作区提交到暂存区

```bash
git add 文件名
```

#### 用暂存区覆盖工作区（撤销修改）

```bash
git checkout 文件名
```

#### 提交修改到分支

```bash
git commit -m "备注"
```

#### 查看git状态

- ##### 查看被修改文件

  ```bash
  git status
  ```

- ##### 查看修改内容

  1. ###### 工作区与暂存区比较

     ```bash
     git diff
     ```

  2. ###### 暂存区与分支比较

     ```bash
     git diff -cache
     ```

- ##### 查看某次修改

  ```bash
  git show commit_id
  ```

- ##### 查看提交历史

  ```bash
  git log
  ```

- ##### 查看命令历史

  ```bash
  git reflow
  ```

#### 连上远程仓库

```bash
#origin远程仓库在本地的别名
#gitlink远程仓库链接
git remote add origin gitlink 
```

#### 拉取远程分支内容

```bash
git pull (--rebase)
```

- git pull时可以加上--rebase参数, 使之不产生Merge点, 保证了代码的整洁

#### 推送分支内容

```bash
#origin要推送到的远程仓库在本地的别名
#dev要被推送的本地分支
#dev_r要推送到的远程分支
git push -u origin dev:dev_r 
```

```bash
#origin要推送到的远程仓库在本地的别名
#dev要被推送的本地分支
#dev_r要推送到的远程分支
git branch -u origin dev:dev_r 
```

- 举例

  ```bash
  git push -u origin master：main
  ```

- git push -u 与 git push -u的区别？

  ```bash
  git push -u origin dev = git push origin/dev dev + git branch -u origin/dev dev 
  ```

- git push -u origin 与 git branch -u origin的区别？
  git push origin不指定远程分支,则默认的远程分支与本地分支一样
  git branch origin不指定远程分支,则默认的远程分支=master

  - 举例

    ```bash
    git push origin dev = git push origin/dev dev
    ```

    ```bash
    git branch origin dev = git branch origin/master dev
    ```

#### 生成SSH密钥

```bash
#配置用户名
git config --global user.name "username"
```

```bash
#配置用户邮箱
git config --global user.email "useremail"
```

```bash
#生成SSH公钥和私钥
ssh-keygen -t rsa -C "useremail"
```

```bash
#查看公钥
cat ~/.ssh/id_rsa.pub
#查看私钥
cat ~/.ssh/id_rsa
```

