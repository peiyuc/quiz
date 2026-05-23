# 三年级下册字词句专项练习

纯前端静态应用，支持看拼音写字、看字写拼音、句子填空等练习模式，内置错题本功能。

## 本地预览

```bash
npm run dev
```

或直接打开 `public/index.html`。

## 部署到 Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/your-username/your-repo)

或连接 GitHub 仓库后，Vercel 会自动识别 `public/` 目录并部署。

## 目录结构

```
public/
  ├── index.html    # 入口页面
  └── data.js       # 题库数据
```

## 技术说明

- 纯静态站点，无后端依赖
- 错题数据存储在浏览器 `localStorage` 中
- 如需云端同步，可后续扩展 `api/` 目录接入 Vercel Serverless Functions
