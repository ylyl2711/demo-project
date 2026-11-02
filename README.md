# 我的第一个仓库 · 个人主页

> 第10周课堂样例项目：用 Trae 生成 → 用 Git 管理 → 用 GitHub Pages 发布


仓库地址：<https://github.com/ylyl2711/demo-project>

## 功能清单

- 顶部个人介绍横幅
- 个人信息卡片（姓名 / 班级 / 学号）
- 课程清单表格（由 JavaScript 渲染）
- 点赞按钮交互
- 页面加载时间显示

## 技术栈

- Vite 5
- 原生 HTML + CSS + JavaScript（无框架，方便看懂）
- ECharts 6（已安装，可用于后续的图表展示）

## 项目结构

```text
demo-project/
├── index.html        # 页面结构
├── src/
│   ├── main.js       # 页面逻辑（数据渲染、交互）
│   └── style.css     # 页面样式
├── vite.config.js    # Vite 配置（base: './'，适配 GitHub Pages）
├── package.json      # 依赖与脚本
└── dist/             # 打包产物（已在 .gitignore 中忽略）
```

## 本地运行

```bash
npm install
npm run dev
```

浏览器打开终端里显示的地址（通常是 http://localhost:5173）。

## 打包与预览

```bash
npm run build    # 产物在 dist 目录
npm run preview  # 本地预览打包结果
```

## 部署到 GitHub Pages

```bash
npm run deploy
```

`gh-pages` 已作为开发依赖安装，命令会自动把 `dist` 推送到 `gh-pages` 分支。
然后到 GitHub 仓库 → Settings → Pages：
Source 选 **Deploy from a branch**，分支选 **gh-pages**，目录选 **/(root)**，保存。
等 1–3 分钟即可拿到公网链接。

## 提交与推送

```bash
git add .
git commit -m "描述这次改动"
git push origin main
```

## 依赖说明

| 包名 | 类型 | 用途 |
| --- | --- | --- |
| vite | devDependencies | 开发服务器与打包 |
| gh-pages | devDependencies | 发布到 GitHub Pages |
| echarts | dependencies | 图表库，按需在 `src/main.js` 中引入使用 |

## 开发说明

本项目为前端静态原型，没有后端和数据库。
第 11 周会在本仓库基础上继续迭代，接入数据库做全栈 CRUD。
