# Git 基础命令速查

## 一次性配置
```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

## 创建仓库
```bash
git init -b main        # 把当前文件夹初始化成 git 项目(本仓库就是这样来的)
git clone <url>         # 把远程仓库克隆到本地
```

## 日常三板斧
```bash
git status              # 查看状态,红色=未暂存,绿色=已暂存
git add <文件>           # 暂存单个文件
git add -A              # 暂存全部改动
git commit -m "提交信息"  # 提交到本地仓库
```

## 远程仓库
```bash
git remote add origin <url>     # 关联远程仓库,起名叫 origin
git remote -v                   # 查看已关联的远程仓库
git push -u origin main         # 第一次推送,并让本地 main 跟踪 origin/main
git push                        # 之后直接 push 即可
git pull                        # 把远程更新拉下来
```

## 分支
```bash
git switch -c <分支名>   # 新建并切换分支
git switch <分支名>      # 切换分支
git merge <分支名>       # 把某分支合并进当前分支
```

## 后悔药
```bash
git log --oneline       # 看提交历史
git restore <文件>      # 丢弃工作区的修改
git restore --staged <文件>  # 取消暂存
```

## 本仓库诞生记(我的第一遍练习流程)
1. `git init -b main`
2. 编写 `README.md`、`.gitignore`、`notes/git-basics.md`
3. `git add -A` && `git commit -m "first commit"`
4. `git remote add origin https://gitee.com/guardian-of-treasures/study-code.git`
5. `git push -u origin main`
6. 关联 GitHub:`git remote add github <url>` && `git push github main`