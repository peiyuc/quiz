# 三年级下册字词句专项练习

纯前端静态应用，支持看拼音写字、看字写拼音、句子填空等练习模式，内置错题本功能。

## 本地预览

直接浏览器打开 `index.html`，或启动本地服务器：

```bash
python3 -m http.server 8081
```

## 部署到 Vercel

1. 把代码推送到 GitHub
2. 在 [Vercel](https://vercel.com/new) 导入仓库
3. Framework Preset 选 **Other**（纯静态）
4. Build Command 留空，Output Directory 留空
5. 点击 Deploy

Vercel 会自动识别根目录的 `index.html` 作为入口。
