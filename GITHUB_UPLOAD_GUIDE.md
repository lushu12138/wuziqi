# GitHub 上传指南

## 第一步：配置 Git 用户信息（如果还没有配置）

在命令行中运行以下命令，替换为你的 GitHub 用户名和邮箱：

```bash
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub邮箱"
```

或者只为这个项目配置（不添加 --global）：

```bash
git config user.name "你的GitHub用户名"
git config user.email "你的GitHub邮箱"
```

## 第二步：在 GitHub 上创建新仓库

1. 登录 GitHub
2. 点击右上角的 "+" 号，选择 "New repository"
3. 填写仓库信息：
   - Repository name: `wuziqi`（或你喜欢的名字）
   - Description: `一个简单的五子棋游戏`
   - 选择 Public（公开）或 Private（私有）
   - **不要**勾选 "Initialize this repository with a README"（因为我们已经有了）
4. 点击 "Create repository"

## 第三步：连接本地仓库到 GitHub

创建仓库后，GitHub 会显示连接命令。在项目目录下运行：

```bash
# 添加远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/你的用户名/wuziqi.git

# 或者使用 SSH（如果你配置了 SSH key）
# git remote add origin git@github.com:你的用户名/wuziqi.git
```

## 第四步：提交代码到 GitHub

```bash
# 查看当前状态
git status

# 添加所有文件到暂存区
git add .

# 提交代码（如果还没有提交）
git commit -m "Initial commit: 五子棋游戏项目"

# 推送到 GitHub（主分支通常是 main 或 master）
git branch -M main
git push -u origin main
```

## 后续提交更多代码（提高分数）

每次修改代码后，重复以下步骤来增加 Commit 数量：

```bash
# 1. 查看修改的文件
git status

# 2. 添加修改的文件
git add .

# 3. 提交更改（使用有意义的提交信息）
git commit -m "更新: 添加新功能/修复bug/优化代码"

# 4. 推送到 GitHub
git push
```

## 提高项目分数的建议

根据评分标准，你可以通过以下方式提高分数：

### 流行程度维度：
1. **增加 Commit 数量**：定期提交代码更改
   ```bash
   # 可以做一些小的改进，比如：
   git commit -m "优化: 改进游戏界面样式"
   git commit -m "功能: 添加游戏音效"
   git commit -m "修复: 修复边界检测bug"
   ```

2. **创建 PR（Pull Request）**：
   - Fork 自己的仓库
   - 创建新分支进行修改
   - 提交 PR 合并到主分支

3. **创建 Issue**：
   - 在 GitHub 仓库页面点击 "Issues"
   - 点击 "New issue"
   - 创建一些功能请求或问题讨论

4. **创建 Release**：
   - 在 GitHub 仓库页面点击 "Releases"
   - 点击 "Create a new release"
   - 填写版本号和发布说明

### 标准程度维度：
✅ 已完成：
- README 文件
- LICENSE 文件
- CONTRIBUTING.md
- CODE_OF_CONDUCT.md
- PR 模板
- Issue 模板

## 常见问题

### 如果推送时要求输入用户名和密码：
- 使用 Personal Access Token 代替密码
- 在 GitHub Settings > Developer settings > Personal access tokens 创建 token

### 如果遇到分支名称问题：
```bash
# 查看当前分支
git branch

# 如果当前是 master，改为 main
git branch -M main

# 或者保持使用 master
git push -u origin master
```

### 查看远程仓库配置：
```bash
git remote -v
```

## 完成！

上传成功后，你的项目就可以在 GitHub 上看到了。记得定期提交代码来增加 Commit 数量，提高项目分数！

