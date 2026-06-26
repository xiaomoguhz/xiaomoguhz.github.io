# xiaomoguhz.github.io

王俊杰 (Wang Junjie) 的个人学术主页，基于 GitHub Pages，纯静态（无构建步骤）。
样式参考 Size Wu / AcademicPages（Minimal Mistakes）：左侧 sticky 头像栏 + 右侧内容，
含近期动态 News 时间线，支持中英双语切换。

在线地址：https://xiaomoguhz.github.io

## 目录结构

```
index.html       # 主页（侧栏 + About / News / Publications / Experience / Projects / Honors / Education + 双语切换 JS）
style.css        # 样式（两栏布局 / 系统 sans-serif / 蓝色链接 / 响应式）
image/
  avatar.svg     # 头像占位（首字母 JW），替换为真实照片
```

社交图标用 Font Awesome 6（CDN 引入），无需本地资源。

## 如何维护

- **头像**：把照片存为 `image/avatar.svg`（或换成 `avatar.jpg` 并同步改 `index.html` 里的 `src`）。建议正方形、≥400px。
- **近期动态 News**：在 `index.html` 的 `<div class="news">` 内按倒序增删 `<p>` 条目，日期格式 `(Mon Year)`。
- **论文 Publications**：在对应 `pubgroup` 下增删 `<div class="pub">` 块。
- **Google Scholar 链接**：`index.html` 侧栏中 `Google Scholar` 的 `href="#"` 是占位，替换为真实主页 URL。
- **News 日期**：当前日期按各会议常规通知期估填，请按实际录用时间核对。

## 本地预览

```bash
cd xiaomoguhz.github.io
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 上线（GitHub Pages）

用户主页仓库命名为 `xiaomoguhz.github.io`，推送到 `main` 分支后，
Pages 自动构建，几分钟后通过 https://xiaomoguhz.github.io 访问。
