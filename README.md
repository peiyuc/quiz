# 小学天天练

纯前端静态单页应用，无后端，数据持久化存于浏览器 `localStorage`。支持语文和数学双学科练习，专为 iPad + Apple Pencil 书写场景优化。

## 功能概览

### 语文（三年级下册）
- **看拼音写字** — 根据拼音在方格内书写词语
- **看字写拼音** — 在四线三格内填写拼音（带虚拟拼音键盘）
- **句子填空** — 根据句子语境填写目标字词
- **每日一练** — 每次随机抽取 10 题，优先出未练习过的词语；支持手动添加自定义题目
- **错题本** — 做错自动收录，支持按错词频次 / 单元顺序 / 随机三种模式复习
- **历史记录** — 保存每次练习成绩和用时

### 数学（口算）
- **每日一练** — 每天 20 题（5 加 / 5 减 / 5 乘 / 5 除），基于日期种子固定生成
- **计时 + 自动批改** — 交卷后立即显示对错和用时
- **历史记录** — 保存每次练习成绩

### 通用
- **学科 Tab 切换** — 语文 / 数学一键切换
- **自动批改开关** — 默认开启，字满自动翻页；可关闭后手动核对
- **Apple Pencil 全面适配** — 所有按钮、输入框、选择器均已增加 `touch-action: manipulation` 等属性，Pencil 可正常点击和书写
- **错题本跨学科分离** — 语文错题和数学错题分开显示，复习时自动切换到对应学科

## 数据

- `data.js` — 三年级下册语文生字词题库，约 400+ 词条
- `localStorage` — 用户数据（错题本、历史记录、自定义题目、自动批改开关状态）

## 本地预览

```bash
python3 -m http.server 8081
```

或直接用浏览器打开 `index.html`。

## 部署

### Vercel（推荐）

1. 把代码推送到 GitHub
2. 在 [Vercel](https://vercel.com/new) 导入仓库
3. Framework Preset 选 **Other**（纯静态）
4. Build Command 留空，Output Directory 留空
5. 点击 Deploy

> Vercel 默认域名在国内可能 DNS 污染，推荐绑定自定义域名。

### Gitee Pages

需要实名认证后才能开启，可作为国内备用部署方案。

## 双仓库推送

```bash
git push origin main   # GitHub
git push gitee main    # Gitee
```

## 技术栈

- HTML5 + CSS3 + Vanilla JS（无框架）
- 单文件架构（`index.html` 含全部逻辑）
- 数据文件 `data.js` 独立加载
- 矢量图标 `favicon.svg`

## 浏览器兼容性

- Safari（iPad 主力推荐）
- Chrome / Edge
- 需支持 `localStorage`、`ES6`
