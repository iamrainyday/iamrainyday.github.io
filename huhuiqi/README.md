# 胡慧琦的学术主页

这是一个基于 Jekyll 构建的精美学术网站，包含以下六个主要部分：

## 📂 网站结构

- **首页 (index.md)** - 个人简介与最新动态
- **研究方向 (research.md)** - 详细的研究领域介绍
- **项目系统 (projects.md)** - 主持和参与的科研项目
- **论文发表 (publications.md)** - 学术论文与成果展示
- **课程 (teaching.md)** - 教学课程与教育理念
- **研究生就业 (students.md)** - 学生就业情况与指导

## 🚀 快速开始

### 本地预览

1. 安装 Jekyll 和依赖：
```bash
gem install jekyll bundler
bundle install
```

2. 启动本地服务器：
```bash
bundle exec jekyll serve
```

3. 在浏览器中访问 `http://localhost:4000/huhuiqi`

### 部署到 GitHub Pages

1. 将代码推送到你的 GitHub 仓库
2. 在仓库设置中启用 GitHub Pages
3. 选择 main 分支作为源
4. 网站将自动部署到 `https://yourusername.github.io/huhuiqi`

## ✏️ 自定义配置

### 修改个人信息

编辑 `_config.yml` 文件中的以下内容：

```yaml
title: 你的姓名的学术主页
author:
  name: 你的姓名
  email: your.email@university.edu
  institution: 你的大学/机构名称
  department: 你的系所
  position: 你的职位
```

### 添加个人头像

将你的头像文件命名为 `profile.jpg` 并放在 `assets/images/` 目录下。
建议尺寸：300x300 像素，正方形。

### 更新内容

- 修改各个 `.md` 文件来更新页面内容
- 在 `assets/css/style.css` 中自定义样式
- 添加更多页面可以在 `_config.yml` 的 `header_pages` 中配置

## 🎨 特色功能

- ✅ 响应式设计，适配桌面和移动设备
- ✅ 现代化的卡片式布局
- ✅ 优雅的导航栏设计
- ✅ SEO 友好的配置
- ✅ 快速加载的静态网站
- ✅ GitHub Pages 原生支持

## 📝 使用提示

1. **内容更新**：直接修改对应的 Markdown 文件即可
2. **样式调整**：编辑 `assets/css/style.css` 文件
3. **添加页面**：创建新的 `.md` 文件并在 `_config.yml` 中配置导航
4. **图片管理**：将图片放在 `assets/images/` 目录下

## 🛠️ 技术栈

- **Jekyll** - 静态网站生成器
- **Markdown** - 内容编写
- **CSS3** - 样式设计
- **GitHub Pages** - 托管部署

## 📞 支持

如果你在使用过程中遇到任何问题，欢迎：

1. 查看 Jekyll 官方文档：https://jekyllrb.com/
2. 参考 GitHub Pages 帮助：https://pages.github.com/
3. 提交 Issue 到项目仓库

---

🎉 现在你已经拥有一个专业的学术网站了！记得定期更新你的研究成果和学术动态。
