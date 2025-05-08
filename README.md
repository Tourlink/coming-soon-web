# Tourlingo Web 项目

## 项目简介
Tourlingo 是一个 AI 驱动的下一代旅行指南 Web 应用，旨在为用户提供更智能、更便捷的旅行体验。

## 主要功能
- 智能旅行推荐
- 旅行路线规划
- 目的地信息展示
- 个性化行程管理
- 响应式设计，适配多终端

## 技术栈
- 前端框架：Next.js 15
- 组件库：shadcn/ui, Radix UI, Tailwind CSS
- 动画与交互：framer-motion
- 其他依赖：react, zod, date-fns 等

## 目录结构说明
- `app/`：页面与路由
- `components/`：UI 组件
- `hooks/`：自定义 React Hooks
- `lib/`：工具函数与库
- `public/`：静态资源
- `styles/`：全局样式

## 快速开始
1. 安装依赖：`pnpm install` 或 `npm install`
2. 本地开发：`pnpm dev` 或 `npm run dev`
3. 构建生产包：`pnpm build` 或 `npm run build`
4. 启动生产环境：`pnpm start` 或 `npm start`

---

## 部署与域名绑定详细教程（适合新手）

### 1. 代码上传到 GitHub
1. 注册并登录 [GitHub](https://github.com)。
2. 新建一个仓库（Repository），如 `tourlingo-web`。
3. 在本地项目根目录打开终端，依次输入：
   ```bash
   git init
   git remote add origin https://github.com/你的用户名/tourlingo-web.git
   git add .
   git commit -m "init"
   git push -u origin master
   ```
   > 如果遇到分支问题，可用 `git push -u origin main`。

### 2. Cloudflare Pages 免费部署
1. 注册并登录 [Cloudflare](https://dash.cloudflare.com/)。
2. 进入 Cloudflare 后台，左侧菜单选择"Pages"。
3. 点击"Create a Project"，选择"Connect to Git"并授权 GitHub。
4. 选择刚刚上传的仓库（如 `tourlingo-web`），点击"Begin setup"。
5. 配置构建设置：
   - Framework preset: 选择 `Next.js`
   - Build command: `npm run build` 或 `pnpm build`
   - Output directory: `.next`
   - Root directory: 留空或填 `/`
6. 点击"Save and Deploy"，等待几分钟，部署成功后会生成一个临时域名（如 `xxx.pages.dev`）。

### 3. 阿里云域名解析到 Cloudflare Pages
1. 登录 [阿里云域名控制台](https://dc.console.aliyun.com/next/index)。
2. 找到你的域名 `tourlingo.cn`，点击"解析"。
3. 添加一条 CNAME 记录：
   - 主机记录：`www`（或留空表示根域名）
   - 记录类型：CNAME
   - 记录值：Cloudflare Pages 分配的临时域名（如 `xxx.pages.dev`）
   - TTL：默认即可
4. 保存后，等待几分钟到半小时，域名即可访问你的站点。

### 4. Cloudflare Pages 绑定自定义域名
1. 回到 Cloudflare Pages 项目设置，选择"Custom domains"。
2. 输入你的域名（如 `tourlingo.cn`），点击"Add"。
3. 按提示完成域名验证（一般只需等待 DNS 生效）。
4. 验证通过后，Cloudflare 会自动为你配置 HTTPS。

---

## 常见问题解答
- **DNS 解析不生效？** 检查 CNAME 是否填写正确，或等待更长时间。
- **GitHub 推送失败？** 检查网络或仓库权限。
- **Cloudflare Pages 构建失败？** 检查构建命令和目录设置。

---

## 联系与反馈
如有疑问，可在 GitHub 提 issue，或联系开发者邮箱。

---

## 未来规划与改进
- 增加多语言支持
- 增强 AI 推荐能力
- 优化移动端体验

---

如有任何问题，请联系开发者或提交 issue。 