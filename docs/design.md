# 设计说明 (Design) - 个人网站

## 1. 页面结构与浏览顺序

```
主页 (About) → Portfolio → Blog Posts → CV
```

1. **主页 (Home / About)** — 欢迎语、个人简介、技能列表、项目展示、联系方式
2. **Portfolio** — 项目作品集展示
3. **Blog Posts** — 博客文章归档
4. **CV** — 个人简历（JSON 数据驱动）

导航栏固定在页面顶部，始终可访问。

## 2. 颜色、字体与整体风格

- **主色调**：深蓝 (#2c3e50) + 白色背景（Academic Pages 默认配色）
- **强调色**：深蓝用于标题和链接，灰色用于辅助文字
- **字体**：系统无衬线字体（Segoe UI / Helvetica / Arial）
- **风格**：简洁、学术、信息密度适中，强调可读性
- **ICON**：Font Awesome 图标，用于社交链接和联系信息

## 3. 移动端与响应式要求

- **桌面端（≥1024px）**：左侧作者侧边栏 + 右侧主内容区双列布局
- **平板端（768-1024px）**：侧边栏折叠为顶部导航
- **手机端（≤768px）**：单列布局，文字自动换行，导航栏折叠为汉堡菜单
- **关键检查**：所有视口均无横向溢出，文字不重叠

## 4. 关键文件映射

| 文件 | 负责内容 |
|------|---------|
| `_config.yml` | 站点全局配置、作者信息、社交链接 |
| `_pages/about.md` | 首页/关于页面内容 |
| `_data/navigation.yml` | 顶部导航栏菜单 |
| `_layouts/single.html` | 单页布局模板 |
| `_includes/masthead.html` | 导航栏 HTML |
| `_includes/author-profile.html` | 侧边栏个人信息 |
| `_sass/` | 样式文件 |
| `assets/css/main.css` | 主样式表 |

## 5. 保留与修改

| 部分 | 处理方式 |
|------|---------|
| 整体布局、响应式机制 | ✅ 保留 |
| Jekyll 构建体系 | ✅ 保留 |
| 个人信息、导航菜单 | ✅ 修改为用户数据 |
| 首页内容 | ✅ 替换为个人简介 |
| 示例 PDF / 占位图片 | ✅ 已删除 |
| 示例发表文章 | ✅ 已清空 |
| GitHub 链接、URL | ✅ 修改为 ruida-so |

## 6. 素材来源

- 头像：profile.png（占位图，后续替换为本人照片）
- 图标：Font Awesome / Academicons（CDN 引用）
- 模板框架：Academic Pages（MIT License）
