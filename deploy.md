# 部署指南

## GitHub + Vercel 部署步骤

### 1. 创建GitHub仓库

```bash
# 初始化Git仓库
git init
git add .
git commit -m "Initial commit: Nuclear Fusion Stocks Landing Page"

# 添加远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/你的用户名/你的仓库名.git
git branch -M main
git push -u origin main
```

### 2. Vercel部署

1. 访问 [Vercel Dashboard](https://vercel.com/dashboard)
2. 点击 "New Project"
3. 选择你的GitHub仓库
4. 配置项目：
   - **Project Name**: nuclear-fusion-stocks-landing
   - **Framework Preset**: Other
   - **Root Directory**: ./ (保持默认)
   - **Build Command**: npm run build
   - **Output Directory**: public
5. 点击 "Deploy"

### 3. 环境变量配置

在Vercel项目设置中添加：

```
ANALYTICS_TRACKING_ID=AW-11435373698/0AA1CJj1oaMbEILp58wq
```

### 4. 自定义域名（可选）

1. 在Vercel项目设置中添加自定义域名
2. 配置DNS记录指向Vercel

## 本地开发

```bash
# 安装Vercel CLI
npm install -g vercel

# 进入项目目录
cd vercel1

# 启动开发服务器
vercel dev
```

## 文件说明

- `index.html`: 主页面（核融合发电股票信息）
- `contact.html`: 跳转页面（LINE链接）
- `assets/`: 静态资源文件夹
- `vercel.json`: Vercel配置文件
- `package.json`: 项目配置文件

## 功能特性

✅ IP地域检测（仅限日本）  
✅ 响应式设计  
✅ Google Analytics跟踪  
✅ LINE自动跳转  
✅ 多色标题设计  
✅ 股票数据展示  

## 注意事项

1. 确保所有资源路径使用相对路径
2. IP检测API可能需要处理CORS问题
3. 建议定期更新股票数据
4. 监控Google Analytics转化数据
