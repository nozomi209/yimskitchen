# Yi's Kitchen - 个人食谱网站

一个完全托管在 GitHub Pages 上的静态食谱网站，使用 Jekyll + Markdown 构建。

## ✨ 特性

- 🎨 现代化、响应式设计
- 📱 移动端友好
- 🚀 完全静态，无需服务器
- 📝 Markdown 格式编写食谱
- 🔍 简单易用的导航
- 🏷️ 标签分类系统

## 🚀 快速开始

### 1. 克隆或下载此仓库

```bash
git clone https://github.com/yourusername/yimskitchen.git
cd yimskitchen
```

### 2. 推送到 GitHub

1. 在 GitHub 上创建一个新仓库（例如：`yimskitchen`）
2. 将代码推送到仓库：

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/yimskitchen.git
git push -u origin main
```

### 3. 启用 GitHub Pages

1. 进入仓库的 **Settings**（设置）
2. 找到 **Pages** 选项
3. 在 **Source** 中选择 **GitHub Actions** 或 **Deploy from a branch**
   - 如果选择 branch，选择 `main` 分支和 `/ (root)` 目录
4. 保存后，GitHub 会自动构建并部署你的网站
5. 几分钟后，你的网站就可以通过 `https://yourusername.github.io/yimskitchen` 访问了

## 📝 添加新食谱

1. 在 `_recipes/` 目录下创建一个新的 Markdown 文件（例如：`宫保鸡丁.md`）
2. 使用以下模板：

```markdown
---
title: "食谱名称"
subtitle: "副标题（可选）"
description: "简短描述"
date: 2024-01-20
servings: 2
prep_time: "10分钟"
cook_time: "20分钟"
image: "/assets/images/recipe-image.jpg"
tags: ["标签1", "标签2"]
---

## 小贴士（可选）

这里可以写一些制作要点或小技巧。

ingredients:
  - "食材1 用量"
  - "食材2 用量"

steps:
  - "步骤1"
  - "步骤2"
  - "步骤3"
```

3. 提交并推送更改：

```bash
git add _recipes/新食谱.md
git commit -m "添加新食谱"
git push
```

GitHub Pages 会自动重新构建网站。

## 🖼️ 添加图片

1. 将图片放在 `assets/images/` 目录下
2. 在食谱的 front matter 中使用相对路径：

```yaml
image: "/assets/images/your-image.jpg"
```

## 🎨 自定义

### 修改网站信息

编辑 `_config.yml` 文件：

```yaml
title: "你的网站名称"
description: "你的网站描述"
url: "https://yourusername.github.io"
baseurl: "/yimskitchen"  # 如果仓库名不是 username.github.io
```

### 修改样式

编辑 `assets/css/style.css` 文件，可以修改颜色、字体等。

### 修改布局

- `_layouts/default.html` - 默认布局
- `_layouts/recipe.html` - 食谱页面布局

## 📁 目录结构

```
yimskitchen/
├── _config.yml          # Jekyll 配置文件
├── _layouts/            # 布局文件
│   ├── default.html
│   └── recipe.html
├── _recipes/            # 食谱 Markdown 文件
│   ├── 番茄鸡蛋面.md
│   ├── 红烧肉.md
│   └── ...
├── assets/
│   └── css/
│       └── style.css    # 样式文件
├── index.html           # 首页
├── recipes.html         # 所有食谱页面
└── README.md           # 说明文档
```

## 🔧 本地开发（可选）

如果你想在本地预览网站：

1. 安装 Ruby 和 Jekyll：

```bash
gem install bundler jekyll
```

2. 安装依赖：

```bash
bundle install
```

3. 启动本地服务器：

```bash
bundle exec jekyll serve
```

4. 在浏览器中访问 `http://localhost:4000`

## 📄 许可证

MIT License - 自由使用和修改

## 🙏 致谢

感谢使用这个模板！希望你能用它记录下每一道美味。

