# Nova AI · 智能对话助手

> 一个基于纯前端的 AI 对话界面，支持 10+ 主流 AI 服务商，无需后端，数据仅在本地处理。

![Nova AI 界面预览](https://hualiu312.github.io/nova-ai/preview.png)

---

## ✨ 功能特性

- **多服务商支持** — 一键切换 Anthropic、OpenAI、DeepSeek、通义千问、Gemini、月之暗面、豆包、Groq、Mistral 等 10+ 服务商
- **模型卡片选择** — 可视化模型选择界面，附带模型特性说明，告别手动输入模型 ID
- **多配置管理** — 同时保存多个 API 配置，随时切换使用
- **对话历史** — 本地保存最近 20 条对话记录，支持随时继续
- **Markdown 渲染** — 支持代码块、粗体、斜体等基础格式化输出
- **深色模式** — 一键切换亮色 / 暗黑主题
- **隐私优先** — 所有数据（API Key、对话记录）仅存储在本地浏览器，不经过任何第三方服务器
- **零依赖部署** — 单个 `index.html` 文件，无需构建工具，开箱即用

---

## 🤖 支持的 AI 服务商

| 服务商 | 推荐模型 | 是否免费 | 获取 Key |
|--------|---------|---------|---------|
| Anthropic | Claude Sonnet 4 | 付费 | [console.anthropic.com](https://console.anthropic.com) |
| OpenAI | GPT-4o | 付费 | [platform.openai.com](https://platform.openai.com) |
| DeepSeek | DeepSeek V3 | 极低价 | [platform.deepseek.com](https://platform.deepseek.com) |
| 通义千问 | Qwen Max | 有免费额度 | [dashscope.aliyuncs.com](https://dashscope.aliyuncs.com) |
| Google Gemini | Gemini 2.0 Flash | **免费** | [aistudio.google.com](https://aistudio.google.com) |
| 月之暗面 | Moonshot 128k | 有免费额度 | [platform.moonshot.cn](https://platform.moonshot.cn) |
| 字节豆包 | Doubao Pro 32k | 极低价 | [console.volcengine.com](https://console.volcengine.com/ark) |
| Groq | Llama 3.3 70B | **完全免费** | [console.groq.com](https://console.groq.com) |
| Mistral | Mistral Large | 付费 | [console.mistral.ai](https://console.mistral.ai) |
| 自定义 | 任意兼容 OpenAI 格式的接口 | — | — |

> 💡 **新手推荐**：Groq 完全免费，注册即用，速度极快，适合入门体验。

---

## 🚀 部署教程

### 方式一：Cloudflare Pages（推荐）

速度最快，全球 CDN 加速，免费，且支持 GitHub 自动同步部署。

**第一步：Fork 仓库**

点击本页右上角 **Fork**，将仓库复制到你自己的 GitHub 账号下。

**第二步：连接 Cloudflare Pages**

1. 登录 [dash.cloudflare.com](https://dash.cloudflare.com)，注册免费账号
2. 左侧菜单点击 **Workers & Pages** → **Create** → **Pages**
3. 选择 **导入现有 Git 存储库**，授权 GitHub 并选择你 Fork 的仓库

**第三步：配置构建设置**

| 字段 | 填写 |
|------|------|
| 框架预设 | 无 |
| 构建命令 | 留空 |
| 构建输出目录 | 留空 |

**第四步：部署**

点击**保存并部署**，等待约 1 分钟，部署完成后即可通过 `your-project.pages.dev` 访问。

> 之后每次向 GitHub 推送代码，Cloudflare Pages 会自动重新部署。

---

### 方式二：GitHub Pages

**第一步：Fork 仓库**

点击右上角 **Fork** 复制仓库。

**第二步：开启 GitHub Pages**

1. 进入你 Fork 的仓库，点击顶部 **Settings**
2. 左侧菜单选择 **Pages**
3. Source 选择 **Deploy from a branch**
4. Branch 选择 `main`，目录选择 `/ (root)`
5. 点击 **Save**

**第三步：访问**

稍等片刻，访问 `https://你的用户名.github.io/nova-ai/` 即可。

---

### 方式三：本地运行

无需任何安装，直接用浏览器打开文件：

```bash
# 克隆仓库
git clone https://github.com/hualiu312/nova-ai.git

# 进入目录，用浏览器打开 index.html
cd nova-ai
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

---

## 📖 使用说明

**添加 API 配置**

1. 点击右上角**模型设置**
2. 点击**添加新配置**
3. 选择 AI 服务商，点击对应模型卡片
4. 填入 API Key（点击「获取 API Key」链接可直接跳转对应平台）
5. 点击**保存配置**

**切换配置**

在「模型配置」弹窗中，点击任意已保存的配置卡片即可切换。

**开始对话**

在底部输入框输入消息，按 `Enter` 发送，`Shift + Enter` 换行。

---

## 🛠 技术栈

- 纯原生 HTML / CSS / JavaScript，无任何框架依赖
- 字体：Noto Serif SC + DM Mono（Google Fonts）
- API 跨域：通过 [corsproxy.io](https://corsproxy.io) 代理解决浏览器 CORS 限制
- 数据存储：浏览器 localStorage

---

## 📄 License

MIT License © 2026 hualiu312
