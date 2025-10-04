# HTML伪装系统 (jpg-web-html)

🎭 **通过图片URL访问HTML内容的演示项目**

## 项目简介

这是一个展示HTML伪装技术的静态网站项目。通过将HTML文件重命名为`.jpg`扩展名，实现了"看似图片链接，实际访问网页"的伪装效果。

## 在线演示

🌐 **GitHub Pages**: [https://username.github.io/jpg-web-html](https://username.github.io/jpg-web-html)

### 演示文件

- [demo1.jpg](https://username.github.io/jpg-web-html/demo1.jpg) - 基础演示页面
- [clash-config.jpg](https://username.github.io/jpg-web-html/clash-config.jpg) - Clash配置管理页面
- [styled-demo.jpg](https://username.github.io/jpg-web-html/styled-demo.jpg) - 样式展示页面

## 技术原理

### 静态版本实现

1. **文件重命名**: 将HTML文件重命名为`.jpg`扩展名
2. **MIME类型检测**: Web服务器根据文件内容而非扩展名确定MIME类型
3. **浏览器解析**: 浏览器检测到HTML内容后自动渲染为网页
4. **静态托管**: 利用GitHub Pages等静态文件托管服务

### 完整版本功能

完整版本需要后端服务支持，可实现：

- ✅ 动态文件上传
- ✅ 自动URL生成
- ✅ 访问统计
- ✅ Base64内容处理
- ✅ 文件管理

## 项目结构

```
jpg-web-html/
├── index.html          # 主页面
├── demo1.jpg          # 基础演示文件
├── clash-config.jpg   # Clash配置演示
├── styled-demo.jpg    # 样式展示演示
└── README.md          # 项目说明
```

## 特性展示

### 🎭 URL伪装
- 文件名以`.jpg`结尾，看起来像图片链接
- 实际包含完整的HTML内容

### 🌐 HTML渲染
- 浏览器访问时渲染为完整的HTML页面
- 支持CSS样式和JavaScript交互

### 📱 响应式设计
- 支持各种设备和屏幕尺寸
- 现代化的用户界面设计

### ⚡ 静态托管
- 可部署在GitHub Pages等静态托管服务
- 无需后端服务器支持

## 使用方法

### 本地运行

1. 克隆项目
```bash
git clone https://github.com/username/jpg-web-html.git
cd jpg-web-html
```

2. 启动本地服务器
```bash
# 使用Python
python -m http.server 8000

# 或使用Node.js
npx serve .
```

3. 访问 `http://localhost:8000`

### GitHub Pages部署

1. Fork本项目
2. 在仓库设置中启用GitHub Pages
3. 选择源分支（通常是`main`或`master`）
4. 访问 `https://yourusername.github.io/jpg-web-html`

## 技术栈

- **前端**: HTML5 + CSS3 + JavaScript
- **样式**: 原生CSS（渐变、动画、响应式）
- **托管**: GitHub Pages
- **版本控制**: Git

## 应用场景

### 📄 内容伪装
- 将敏感内容伪装成普通图片链接
- 避免直接暴露HTML文件

### 🔒 简单保护
- 提供一定程度的内容保护
- 增加访问的隐蔽性

### 🎨 创意展示
- 展示前端技术和创意设计
- 教学演示用途

### 📱 兼容性测试
- 测试不同浏览器的MIME类型处理
- 验证静态托管服务的行为

## 浏览器兼容性

| 浏览器 | 版本 | 支持状态 |
|--------|------|----------|
| Chrome | 60+ | ✅ 完全支持 |
| Firefox | 55+ | ✅ 完全支持 |
| Safari | 12+ | ✅ 完全支持 |
| Edge | 79+ | ✅ 完全支持 |
| IE | 11 | ⚠️ 部分支持 |

## 注意事项

### 限制说明

- **静态特性**: GitHub Pages版本无法实现动态文件上传
- **MIME依赖**: 依赖服务器的MIME类型检测机制
- **SEO影响**: 搜索引擎可能无法正确索引伪装的内容

### 安全考虑

- 这种伪装方式仅提供表面的隐藏效果
- 不应用于真正的安全敏感场景
- 技术人员仍可轻易识别文件的真实内容

## 贡献指南

欢迎提交Issue和Pull Request！

1. Fork项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 联系方式

- 项目主页: [https://github.com/username/jpg-web-html](https://github.com/username/jpg-web-html)
- 问题反馈: [Issues](https://github.com/username/jpg-web-html/issues)

## 致谢

感谢所有为这个项目提供想法和反馈的朋友们！

---

⭐ 如果这个项目对您有帮助，请给它一个星标！
