# 鸟类预习 App —— 部署教程

一个网页版鸟类闪卡工具：粘贴「内容链接」加载鸟图+鸟名，刷闪卡、收藏到题库、按题库复习。手机和电脑浏览器都能用。

## 一、文件说明

```
bird-cards/
├── index.html          ← 网页 App（这是主体）
└── content/
    └── birds.json      ← 内容文件（鸟图+鸟名，可多个）
```

## 二、部署到 GitHub Pages（免费，一次配置，永久使用）

### 第 1 步：新建仓库

1. 打开 https://github.com ，登录你的账号
2. 点右上角 **「+」→ New repository**
3. 仓库名填 `bird-cards`，选 **Public（公开）**，点 **Create repository**

### 第 2 步：上传文件

在新建的仓库页里：

1. 点 **「uploading an existing file」**（或 Add file → Upload files）
2. 把本地的 **`index.html`** 拖进去
3. 点 **Commit changes** 提交
4. 再点 **Add file → Create new file**，路径填 `content/birds.json`
5. 用记事本打开本地 `content/birds.json`，全选复制，粘贴到网页里，点 **Commit**

> 简单做法：也可以一次拖拽 `index.html` + `content` 文件夹一起上传（GitHub 会保留文件夹结构）。

### 第 3 步：开启 Pages

1. 仓库页点 **Settings** → 左侧 **Pages**
2. **Source** 选 **Deploy from a branch**
3. **Branch** 选 **main**，文件夹选 **/ (root)**，点 **Save**
4. 等约 1 分钟，页面顶部会显示网址：
   ```
   https://你的用户名.github.io/bird-cards/
   ```
   这就是你的**网页地址**。

### 第 4 步：拿到内容链接

1. 在仓库里点进 `content` → 点 `birds.json`
2. 点右侧 **Raw** 按钮（或 Download 旁的 Raw）
3. 复制浏览器地址栏的链接，形如：
   ```
   https://raw.githubusercontent.com/你的用户名/bird-cards/main/content/birds.json
   ```

## 三、开始使用

1. 用手机或电脑浏览器打开网页地址（`https://你的用户名.github.io/bird-cards/`）
2. 把**内容链接**粘贴到「内容链接」框，点 **加载**
3. 加载成功后就出现在「历史记录」里，点 **刷闪卡** 开始

## 四、以后怎么更新内容

- 想加一组新鸟：把新的内容文件（JSON）上传到 `content/` 目录，拿到它的 Raw 链接，在网页里粘贴加载即可——**每组独立，互不覆盖**。
- 每组都会保存在「历史记录」里，可随时分开调用。
- 内容文件的格式（JSON）：

```json
{
  "name": "这一组的名字",
  "cards": [
    { "name": "黄胸柳莺", "image": "data:image/png;base64,……" },
    { "name": "栗啄木鸟", "image": "data:image/png;base64,……" }
  ]
}
```

> 你以后把鸟图+名字发给我，我帮你生成新的内容文件，你只需上传并粘贴链接即可。
