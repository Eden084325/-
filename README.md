# 啃料 10 · NPR 英语精修

基于尚雯婕「啃料」四步法的英语学习网页应用：选材料 → 逐字听写 → 通篇背诵 → 背到与原声同速。视觉对标 CNN 10。

这是一个**单文件网页应用**（`index.html`），所有数据保存在你自己浏览器里，不上传任何服务器。

---

## 一、把它发布到 GitHub（最简单的方法：网页拖拽）

1. 打开 https://github.com ，登录（没有账号先免费注册）。
2. 右上角 **+ → New repository**。
   - Repository name 填一个名字，例如 `kenliao`。
   - 选 **Public**（公开，GitHub Pages 免费版需要公开）。
   - 点 **Create repository**。
3. 在新仓库页面点 **uploading an existing file**（或 Add file → Upload files）。
4. 把这个文件夹里的 **`index.html`** 和 **`.nojekyll`** 两个文件一起拖进去。
   -（`.nojekyll` 是隐藏文件，若拖不进去可忽略，一般也能正常发布。）
5. 下方点 **Commit changes**。

## 二、开启 GitHub Pages（得到一个网址，任何电脑/手机都能打开）

1. 进入仓库的 **Settings → Pages**。
2. **Source** 选 `Deploy from a branch`。
3. Branch 选 `main`，文件夹选 `/ (root)`，点 **Save**。
4. 等 1–2 分钟，页面上方会出现你的网址，形如：
   `https://你的用户名.github.io/kenliao/`
5. 打开这个网址就是你的 app 了。收藏它，换电脑直接访问即可。

---

## 三、以后怎么更新？（GitHub 不会自动同步本地改动）

每次我给你新版 `index.html` 后：

1. 进入 GitHub 仓库，点开 `index.html`。
2. 右上角铅笔图标旁的 **···** → 或直接 **Add file → Upload files**，把新的 `index.html` 拖进去覆盖。
3. **Commit changes**。
4. GitHub Pages 会在**一两分钟内自动重新发布**，刷新网址即可看到新版。

> 只有「重新发布」是自动的；「把新文件传上去」这一步每次都要手动做一次。

---

## 四、关于数据（重要）

- 学习进度、笔记、计时存在**每台设备各自的浏览器**里，换设备**不会自动同步**。
- 换设备延续进度：在 app 里用 **导出进度** 存一个 `.json`，到新设备 **导入进度**。
- 音频文件（**OGG / WAV**，不支持 MP3）不随进度备份，需在各设备重新载入。
- 好消息：发布成网址（https）后，音频存储（IndexedDB）能长期保留，比双击打开本地文件更稳。

---

## 可选：用命令行发布（懂 git 的话）

```bash
cd 这个文件夹
git init
git add .
git commit -m "啃料10 英语学习 app"
git branch -M main
git remote add origin https://github.com/你的用户名/kenliao.git
git push -u origin main
```

之后每次更新：`git add . && git commit -m "update" && git push`，Pages 自动重新发布。
