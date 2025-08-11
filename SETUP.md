# GitHub Profile 配置指南

## 🚀 快速开始

### 1. 更新GitHub Profile

```bash
# 在博客项目根目录下运行
npm run profile:update
```

### 2. 配置GitHub Secrets

在GitHub仓库 `learnerjunjun/learnerjunjun` 的 Settings > Secrets and variables > Actions 中添加：

| Secret Name | 描述 | 如何获取 |
|------------|------|---------|
| `METRICS_TOKEN` | GitHub个人访问令牌 | [创建令牌](https://github.com/settings/tokens) |

### 3. 权限配置

**METRICS_TOKEN 需要的权限：**
- `public_repo` (访问公共仓库)
- `read:user` (读取用户信息)
- `read:org` (读取组织信息)
- `repo:status` (访问提交状态)

## 📋 功能说明

### 🔄 自动化功能

| 功能 | 更新频率 | 说明 |
|------|---------|------|
| 博客文章列表 | 每小时 | 从RSS源自动获取最新文章 |
| 贪吃蛇动画 | 每天 | 基于GitHub贡献图生成 |
| GitHub指标 | 每天 | 生成详细的统计报告 |

### 🎨 自定义内容

1. **个人信息**
   - 编辑 `README.md` 中的个人介绍
   - 修改技术栈图标
   - 调整联系方式

2. **视觉效果**
   - 替换 `assets/` 目录中的图片
   - 修改配色主题
   - 调整布局样式

3. **博客集成**
   - 确认RSS源 `https://jingvc.com/atom.xml` 可访问
   - 修改 `.github/workflows/blog-post-workflow.yml` 中的feed_list

## 🛠️ 高级配置

### 添加Spotify音乐展示

1. 获取Spotify用户名
2. 在README.md中更新相应部分
3. 配置Spotify API (可选)

### 自定义Metrics配置

编辑 `.github/workflows/metrics.yml` 文件：

```yaml
plugin_languages_limit: 8  # 显示的语言数量
plugin_isocalendar_duration: half-year  # 日历显示时长
```

### 主题自定义

所有组件都支持主题切换，当前使用 `tokyonight` 主题。

可选主题：
- `dark`
- `radical` 
- `merko`
- `gruvbox`
- `tokyonight`
- `onedark`
- `cobalt`
- `synthwave`

## 🔧 故障排除

### 常见问题

1. **贪吃蛇动画不显示**
   - 检查GitHub Actions是否正常运行
   - 确认有足够的GitHub贡献记录

2. **博客文章不更新**
   - 验证RSS源是否可访问
   - 检查workflow权限设置

3. **Metrics不生成**
   - 确认METRICS_TOKEN正确配置
   - 检查令牌权限是否足够

### 调试方法

1. 查看GitHub Actions日志
2. 检查仓库Secrets配置
3. 验证RSS源格式

## 📚 参考资源

- [Awesome GitHub Profile README](https://github.com/abhisheknaiidu/awesome-github-profile-readme)
- [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)
- [Metrics文档](https://github.com/lowlighter/metrics)

## 💡 最佳实践

1. **定期更新内容** - 保持README的时效性
2. **适度使用动画** - 避免过于花哨影响加载速度
3. **移动端适配** - 确保在各种设备上显示正常
4. **性能优化** - 合理使用第三方服务，避免加载缓慢
