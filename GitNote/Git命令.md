# Git命令</br>
---

# 1、提交本地代码进Github仓库： </br>

> # 第一次

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



> # 第二次

1. 添加文件：
```
git add .或者git add 文件名或者git add *
```
2. 提交代码：
```
git commit -m "提交描述"
``` 
3. 推送更改（本地仓库中）到 GitHub：
```
git push -u origin main
```




### 出错类型

**问题1:**

    ! [rejected]main -> main (non-fast-forward)
    error: failed to push some refs to 'https://github.com/gzxn/notebook.git'
    hint: Updates were rejected because the tip of your current branch is behind
    hint: its remote counterpart. Integrate the remote changes (e.g.
    hint: 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.


**解决命令：** 输入
```
git pull --rebase origin main
```
后，再按第二次操作










</br>
</br>



## 2、删除github仓库文件
<br>

1. 进入需要删除github仓库中代码的本地文件目录(如g盘)删除test.md文件：
```
cd /g/学习/笔记本/Java语言程序设计/JavaNote
```
2. 删除文件：
```
git rm -r test.md
``` 

3. 提交更改：
```
git commit -m "remove test.md"
```


4. 推送更改（本地仓库中）到 GitHub：
```
git push -u origin main
```

<br>
<br>

## 3、重命名GitHub文件
<br>

1. 进入需要重命名github仓库中代码的本地文件目录(如g盘)重命名test.md文件：
```
cd /g/学习/笔记本/Java语言程序设计/JavaNote
```
2. 重命名文件：
<br>
格式：
    git mv old_filename new_filename
    git mv 'old_filename' 'new_filename'
    git mv "old_filename" "new_filename"  

<br>

```
git mv 'chapter 5.1、static关键字.md' 'Chapter 5.1、static关键字.md'
``` 

3. 提交更改：
```
git commit -m "rename chapter 5.1、static关键字.md -> Chapter 5.1、static关键字.md"
```


4. 推送更改（本地仓库中）到 GitHub：
```
git push -u origin main
```


<br>
<br>

## 回退版本（待更新）


<br>
<br>
<br>

## 其他
<br>

显示origin与branch：
```
git remote show branch
```




删除分支：
```
git branch -d BranchName
```









