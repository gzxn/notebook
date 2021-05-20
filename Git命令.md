# Git命令</br> #
---

提交本地代码进git仓库：</br>

> # 第一次 #

1. 将本地目录初始化为 Git 仓库：
```
git init -b main
```

2. 在新的本地仓库中添加文件：
```
git add .
```

3. 提交暂存在本地仓库中的文件：
```
git commit -m "First commit"
```

4. 更改分支为main：
```
git branch -M main
```

5. 添加远程仓库的 URL：
```
git remote add origin  <REMOTE_URL> 
```

6. 推送更改（本地仓库中）到 GitHub：
```
git push -u origin main
```



> # 第二次 #

1. 添加文件：
```
git add *或者git add 文件名
```
2. 提交代码：
```
git commit -m "提交描述"
``` 
3. 推送更改（本地仓库中）到 GitHub：
```
git push -u origin main
```




### 出错类型 ###

**问题1:**

    ! [rejected]main -> main (non-fast-forward)
    error: failed to push some refs to 'https://github.com/gzxn/notebook.git'
    hint: Updates were rejected because the tip of your current branch is behind
    hint: its remote counterpart. Integrate the remote changes (e.g.
    hint: 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.


**解决命令：** 
```
git pull --rebase origin main
```

