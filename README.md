# Learn Arduino — 中文版本地克隆

这是 https://learn-arduino-red.vercel.app/zh/ 的完整本地静态克隆，可离线运行。

## 如何运行

本站是 Vite 构建的 SPA，必须通过 HTTP 服务器访问（直接双击 index.html 无效）。

任选一种方式，在本目录下启动：

```bash
# 方式一：Python（推荐，无需安装额外依赖）
python -m http.server 8123

# 方式二：Node.js
npx http-server -p 8123

# 方式三：VS Code 用户
# 安装 "Live Server" 扩展 → 右键 zh/index.html → Open with Live Server
```

然后浏览器打开：

- 中文版首页：<http://127.0.0.1:8123/zh/>
- 根路径 <http://127.0.0.1:8123/> 会自动跳转到中文版

## 目录结构

```
learn-arduino-local/
├── index.html          # 根路径跳转页（指向 /zh/）
├── zh/index.html       # 中文版页面（唯一 HTML，SPA）
├── assets/             # 全部静态资产
│   ├── index-DOAqqu4h.js    # 入口加载器（语言检测/跳转）
│   ├── main-CETici_M.js     # 主程序
│   ├── stage-TzJN9SKx.js    # 3D 引擎（three.js，程序化建模，无模型文件）
│   ├── kit-D7LqvkTA.js      # 课程数据 + 组件库
│   ├── thumbs-D4q1El81.js   # 课程缩略图
│   ├── zh-DawrnNnG.js       # 中文语言包（其余 11 种语言包也已包含）
│   ├── index-Db24VE9E.css   # 全部样式
│   └── *.woff2              # 24 个字体文件（Barlow / JetBrains Mono / Noto Sans）
├── favicon.ico / favicon.svg / apple-touch-icon.png
├── icon-192.png / icon-512.png / icon-maskable-512.png
└── site.webmanifest    # PWA 清单
```

## 完整性说明

- 站点为单页应用，全部功能（16 节课程、3D 模拟器、代码运行）都在上述 JS 分块中
- 已用浏览器实测：页面所有资源 HTTP 200，零 404；3D 开发板正常渲染；课程可正常切换
- 3D 模型为代码程序化生成，不依赖外部模型文件

## 声明与致谢

- 本仓库是原站的**本地离线学习克隆**，非官方项目
- 原站设计与开发：**Dilum Sanjaya**（[x.com/DilumSanjaya](https://x.com/DilumSanjaya) · [github.com/dilums](https://github.com/dilums)）
- 原站地址：<https://learn-arduino-red.vercel.app/>（请优先访问原站支持作者）
- 本仓库仅供个人学习与离线使用；如原作者认为不妥，将立即删除
