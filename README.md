# TechInnovate 项目

## GitHub 远程仓库连接指南

### 1. 准备工作
- 确保已安装Git（[下载地址](https://git-scm.com/downloads)）
- 拥有GitHub账号（[注册地址](https://github.com/signup)）

### 2. 创建新仓库
1. 登录GitHub
2. 点击右上角"+" → "New repository"
3. 填写仓库名称（如TechInnovate）
4. 选择"Public"或"Private"
5. 点击"Create repository"

### 3. 本地Git初始化
```bash
# 进入项目目录
cd your-project-folder

# 初始化Git仓库
git init

# 添加所有文件到暂存区
git add .

# 提交更改
git commit -m "初始提交"
```

### 4. 连接远程仓库
```bash
# 添加远程仓库（替换YOUR-USERNAME）
git remote add origin https://github.com/YOUR-USERNAME/TechInnovate.git

# 验证远程仓库
git remote -v
```

### 5. 推送代码
```bash
# 首次推送（设置上游分支）
git push -u origin main

# 后续推送
git push
```

### 常见问题
1. 认证失败：
   - 使用SSH密钥或GitHub Token
   - 生成SSH密钥：`ssh-keygen -t ed25519 -C "your_email@example.com"`

2. 冲突解决：
```bash
# 拉取远程更改
git pull origin main

# 解决冲突后重新提交
git add .
git commit -m "解决冲突"
git push
```

## 项目启动
```bash
pnpm install
pnpm dev
```