# 部署指南

本文档详细说明了如何将 `jpg-web-html` 项目部署到 GitHub Pages 和 Cloudflare Pages，并配置自定义域名 `jpgtohtml.zzrbk.xyz`。

## GitHub Pages 部署

### 1. 启用 GitHub Pages

1. 访问 GitHub 仓库：[https://github.com/beibing173/jpg-web-html](https://github.com/beibing173/jpg-web-html)
2. 点击 **Settings** (设置) 选项卡
3. 在左侧导航栏中找到 **Pages** (页面)
4. 在 **Build and deployment** 部分：
   - **Source**: 选择 `Deploy from a branch`
   - **Branch**: 选择 `master`
   - **Folder**: 选择 `/ (root)`
5. 点击 **Save** (保存)

### 2. 配置自定义域名

GitHub Pages 会自动检测到 `CNAME` 文件中的域名 `jpgtohtml.zzrbk.xyz`，并在部署完成后自动配置。

**访问链接**：
- 主域名：[https://jpgtohtml.zzrbk.xyz](https://jpgtohtml.zzrbk.xyz)
- GitHub Pages：[https://beibing173.github.io/jpg-web-html](https://beibing173.github.io/jpg-web-html)

## Cloudflare Pages 部署

### 1. 连接 GitHub 仓库

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 进入 **Pages** 部分
3. 点击 **Create a project**
4. 选择 **Connect to Git**
5. 选择 GitHub 并授权访问
6. 选择 `beibing173/jpg-web-html` 仓库

### 2. 配置构建设置

- **Project name**: `jpg-web-html`
- **Production branch**: `master`
- **Build command**: 留空（静态网站无需构建）
- **Build output directory**: `/`

### 3. 部署项目

点击 **Save and Deploy**，Cloudflare Pages 将自动部署项目。

**访问链接**：
- Cloudflare Pages：[https://jpg-web-html.pages.dev](https://jpg-web-html.pages.dev)

### 4. 配置自定义域名（可选）

如果您希望通过 Cloudflare Pages 使用自定义域名：

1. 在 Cloudflare Pages 项目设置中
2. 进入 **Custom domains** 部分
3. 添加 `jpgtohtml.zzrbk.xyz`
4. 按照提示配置 DNS 记录

## DNS 配置

### 为 GitHub Pages 配置 DNS

在您的 DNS 提供商（如 Cloudflare DNS）中添加以下记录：

```
类型: CNAME
名称: jpgtohtml.zzrbk.xyz (或 @)
值: beibing173.github.io
```

### 为 Cloudflare Pages 配置 DNS

如果使用 Cloudflare Pages 作为主要服务：

```
类型: CNAME
名称: jpgtohtml.zzrbk.xyz (或 @)
值: jpg-web-html.pages.dev
```

## 验证部署

部署完成后，您可以通过以下链接验证：

### 主页面
- [https://jpgtohtml.zzrbk.xyz](https://jpgtohtml.zzrbk.xyz)
- [https://beibing173.github.io/jpg-web-html](https://beibing173.github.io/jpg-web-html)
- [https://jpg-web-html.pages.dev](https://jpg-web-html.pages.dev)

### 演示文件（HTML伪装为图片）
- [https://jpgtohtml.zzrbk.xyz/demo1.jpg](https://jpgtohtml.zzrbk.xyz/demo1.jpg)
- [https://jpgtohtml.zzrbk.xyz/clash-config.jpg](https://jpgtohtml.zzrbk.xyz/clash-config.jpg)
- [https://jpgtohtml.zzrbk.xyz/styled-demo.jpg](https://jpgtohtml.zzrbk.xyz/styled-demo.jpg)

## 更新部署

### 更新 GitHub Pages

1. 修改本地文件
2. 提交并推送到 `master` 分支：
   ```bash
   git add .
   git commit -m "Update content"
   git push origin master
   ```
3. GitHub Pages 将自动重新部署

### 更新 Cloudflare Pages

Cloudflare Pages 会自动监听 GitHub 仓库的变化，当您推送新的提交到 `master` 分支时，会自动触发重新部署。

## 故障排除

### GitHub Pages 常见问题

1. **部署失败**：检查 `CNAME` 文件格式是否正确
2. **自定义域名不工作**：确保 DNS 记录已正确配置并已生效
3. **HTTPS 证书问题**：等待 GitHub 自动颁发 SSL 证书（可能需要几分钟到几小时）

### Cloudflare Pages 常见问题

1. **构建失败**：确保没有设置不必要的构建命令
2. **域名配置问题**：检查 Cloudflare DNS 设置
3. **缓存问题**：在 Cloudflare Dashboard 中清除缓存

## 监控和分析

### GitHub Pages

GitHub Pages 提供基本的流量统计，可在仓库的 **Insights** > **Traffic** 中查看。

### Cloudflare Pages

Cloudflare Pages 提供详细的分析数据，包括：
- 页面访问量
- 带宽使用情况
- 响应时间
- 地理分布

可在 Cloudflare Dashboard 的 Pages 项目中查看这些数据。

## 安全考虑

1. **HTTPS**: 两个平台都自动提供 HTTPS 支持
2. **DDoS 保护**: Cloudflare Pages 提供内置的 DDoS 保护
3. **访问控制**: 可以通过 Cloudflare 设置访问规则和防火墙

## 成本

- **GitHub Pages**: 完全免费（公共仓库）
- **Cloudflare Pages**: 免费套餐包含充足的带宽和构建时间

## 备份策略

1. **源代码备份**: GitHub 仓库本身就是备份
2. **多平台部署**: 同时使用 GitHub Pages 和 Cloudflare Pages 提供冗余
3. **定期导出**: 定期下载网站内容作为本地备份
