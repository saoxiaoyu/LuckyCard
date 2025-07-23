# LuckyCard
### 源代码使用
本文将指导用户如何使用LuckyCard的源代码，并将其定制为自己的个人名片网站。整个过程无需复杂的开发环境，仅需一个文本编辑器即可完成。

---

#### **第一步：获取项目文件**
首先，获取本项目的完整源代码文件，其主要结构如下：
* `index.html`：网站的主体结构和全部内容。
* `style.css`：网站的样式文件。
* `script.js`：网站的交互逻辑文件。
* `assets/`：存放静态资源的文件夹，内部包含：
    * `images/`：存放头像、图标等图片。
    * `files/`：存放PDF简历文件。

---

#### **第二步：修改个人内容 (`index.html`)**
用任意文本编辑器（如 Visual Studio Code, Sublime Text, or Notepad++）打开 `index.html` 文件，根据以下指引修改其中的内容。

1.  **修改头部信息 (`<head>`)**
    * 将 `<title>王宇's个人信息电子名片</title>` 中的“王宇”替换为您的名字。

2.  **修改侧边栏信息 (`<aside class="sidebar">`)**
    * **头像**：替换 `assets/images/my-avatar.png` 文件为您自己的头像图片。
    * **姓名与职位**：修改 `<h1 class="name">王宇</h1>` 和 `<p class="title">冶金工程专业学生</p>`。
    * **联系方式**：在 `<ul class="contacts-list">` 中，逐一修改邮箱、电话、出生年月和籍贯等信息。
    * **社交链接**：在 `<ul class="social-list">` 中，将 `href` 属性值替换为您自己的微信二维码链接和GitHub主页链接。

3.  **修改主内容区 (`<div class="main-content">`)**
    * **关于我**：在 `<article data-page="about">` 中，修改个人自述段落、个人标签以及老师评价部分的内容和图片。
    * **荣誉集/作品集/经历集**：在对应的 `<article>` 标签下，每个 `<li class="project-item">` 代表一个项目。您需要修改其中的：
        * `<a>` 标签的 `href` 链接。
        * `<img>` 标签的 `src` 图片地址。
        * `<h3 class="project-title">` 的项目标题。
    * **公众号/博客**：在 `<article data-page="blog">` 中，修改每个 `<li class="blog-post-item">` 里的文章链接、封面图、标题和摘要。

4.  **替换简历文件**
    * 将您自己的简历PDF文件放入 `assets/files/` 文件夹中。
    * 修改 `index.html` 文件底部的 `<a href="./assets/files/王宇简历.pdf" ...>`，确保 `href` 指向您的简历文件名。

---

#### **第三步：自定义样式 (可选)**
如果您想更改网站的颜色主题或字体等视觉样式，可以编辑 `style.css` 文件。
* **主题颜色**：在文件顶部的 `:root` 选择器中，定义了大量的CSS变量，如 `--bg-gradient-onyx` (背景渐变) 和 `--orange-yellow-crayola` (主色调)。 修改这些变量的值，即可轻松改变整个网站的配色方案。

---

#### **第四步：本地预览与部署**
1.  **本地预览**：完成修改后，直接在您的网页浏览器中打开 `index.html` 文件，即可预览您的个人网站。
2.  **部署上线**：将包含所有修改后文件和 `assets` 文件夹的整个项目，上传到任意静态网站托管服务（如 GitHub Pages, Vercel, Netlify），即可将您的电子名片发布到互联网上。
