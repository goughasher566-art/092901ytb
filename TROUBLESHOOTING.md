# 故障排除指南

## Vercel部署常见问题

### 1. 配置错误：routes 和 headers 冲突

**错误信息：**
```
If 'rewrites', 'redirects', 'headers', 'cleanUrls' or 'trailingSlash' are used, then 'routes' cannot be present.
```

**解决方案：**
- 使用 `rewrites` 替代 `routes`
- 简化 `vercel.json` 配置
- 当前配置已修复

### 2. 缺少public目录错误

**错误信息：**
```
Error: No Output Directory named "public" found after the build
```

**解决方案：**
- 所有静态文件已移动到 `public/` 目录
- `vercel.json` 中指定了 `outputDirectory: "public"`
- 确保 `public/` 目录包含所有网站文件

### 3. Root Directory 设置

**问题：** 项目无法找到文件

**解决方案：**
- 如果vercel1是仓库根目录，设置 Root Directory 为 `./`
- 如果vercel1是子目录，设置 Root Directory 为 `vercel1`

### 4. 静态资源404错误

**问题：** 图片、CSS、JS文件无法加载

**解决方案：**
- 检查 `assets/` 文件夹是否包含所有资源
- 确认HTML中的路径使用相对路径 `./assets/`
- 确保文件名没有特殊字符

### 5. Google Analytics 不工作

**问题：** 转化跟踪无效

**解决方案：**
- 检查 `ANALYTICS_TRACKING_ID` 环境变量
- 确认ID格式正确：`AW-11435373698/0AA1CJj1oaMbEILp58wq`
- 在Vercel项目设置中添加环境变量

### 6. IP检测失败

**问题：** 所有用户都被拒绝访问

**解决方案：**
- 检查IP检测API是否可访问
- 考虑添加备用IP检测服务
- 在开发模式下测试IP检测功能

## 部署检查清单

### 部署前检查
- [ ] 所有静态文件在 `public/` 目录中
- [ ] `public/assets/` 文件夹包含所有资源
- [ ] HTML中的路径使用相对路径 `./assets/`
- [ ] `vercel.json` 配置正确，包含 `outputDirectory: "public"`
- [ ] Google Analytics ID 已更新
- [ ] 测试IP检测功能

### 部署后检查
- [ ] 网站可以正常访问
- [ ] 所有图片和资源加载正常
- [ ] 按钮点击功能正常
- [ ] IP检测功能工作
- [ ] Google Analytics 跟踪正常

## 调试模式

在URL后添加 `?debug=1` 可以启用调试模式：
```
https://your-domain.vercel.app/?debug=1
```

调试模式会显示：
- IP检测状态
- 按钮绑定状态
- 控制台日志信息

## 联系支持

如果问题仍然存在：
1. 检查Vercel部署日志
2. 使用浏览器开发者工具查看控制台错误
3. 确认所有环境变量设置正确
