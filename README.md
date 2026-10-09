# 英语闯关实验室 · Drive English Lab

儿童英语闯关游戏（网页版）：**100 个模块 × 每模块 10 个游戏关卡 = 1000 关**，1036 个单词 / 225 个句型。

**线上地址**：https://linzxl93-glitch.github.io/drive-english-lab/

## 玩法闭环

```
玩关卡(5题) → 答对得🪙 → 过关得首通奖励🪙
    → 模块10关全过 = 通关 → 大奖🪙 + 解锁下一模块
    → 通关的模块，它的专属车车就能用金币兑换
```

- 每模块 10 关 = 10 种玩法：听音找图 / 记忆配对 / 救小鸟拼词 / 看图选词 / 句子拼图 / 听音选中文 / 听指令 / 字母排序 / 打地鼠 / Boss 混合挑战
- 100 辆专属交通工具（含手绘 SVG 坦克、潜水艇、热气球等）
- 5 档稀有度随级别递增：L1 普通 → L5 传说
- 家长模式：一键解锁全部模块（首页底部）

## 技术形态

- **单文件** `index.html`（零依赖、零构建），原生 HTML / CSS / JS
- **PWA**：`manifest.webmanifest` + `sw.js`（network-first），可安装到手机主屏、离线可玩
- 进度存 `localStorage`（key: `drive_english_lab_v5`），不发服务器、不收集任何数据
- 发音用 Web Speech API，音效现场合成（Web Audio API），无任何音频文件

## 版本更新

改了 `index.html` 后：同步把 `sw.js` 里的 `VERSION` 加一位，用户端下次联网打开会提示"有新版本"。

## 相关仓库

- `linzxl93-glitch/drive-english` —— 早期单文件版（126KB，线上仍在）
- 本仓库 —— 网页版实验室（闯关 + 金币 + 车库）
- 本地开发目录：`D:/drive-english-lab/`（含 jsdom 冒烟测试 166 条断言）

## 词库标注

`book` = 抄自教材核对版（30 词，含页码）；`draft` = 按模块主题补充的草稿词（1006 词），合并进正式课程前需对照纸质书补 `sourcePage`。
