# xiaomoguhz.github.io

王俊杰 (Wang Junjie) 的个人学术主页，基于 GitHub Pages，纯静态（无构建步骤）。
样式参考 Jon Barron 学术模板，支持中英双语切换。

在线地址（上线后）：https://xiaomoguhz.github.io

## 目录结构

```
index.html            # 主页（内容 + 双语切换 JS）
style.css             # 样式（Lato 字体 / 蓝橙配色 / 响应式）
image/
  avatar.svg          # 头像占位（首字母 JW），替换为真实照片
  papers/             # 每篇论文一张缩略图占位，替换为真实 pipeline 图
    r3bench.svg  mrig.svg  declip.svg  ovdquo.svg
    gdl.svg  calibclip.svg  dytok.svg  ebt.svg
```

## 如何替换占位资源

- **头像**：把照片存为 `image/avatar.svg`（或换成 `avatar.jpg` 并同步修改 `index.html` 里 `src`）。建议正方形、≥400px。
- **论文缩略图**：把对应论文的 pipeline 图存到 `image/papers/<同名>.svg/png`，保持文件名即可，`index.html` 无需改动。
- **Google Scholar 链接**：`index.html` 中 `Google Scholar` 的 `href="#"` 是占位，替换为真实主页 URL。

## 本地预览

```bash
cd xiaomoguhz.github.io
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 上线（GitHub Pages）

用户主页仓库必须命名为 `xiaomoguhz.github.io`，推送到 `main` 分支后，
在仓库 Settings → Pages 选择 `main` 分支根目录，几分钟后即可通过
https://xiaomoguhz.github.io 访问。
