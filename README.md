## Sonic Perpetual Trading UI

一个基于 React Router 的 Sonic 永续合约交易前端项目。

### 部署与访问

- **生产环境（Vercel）**：`https://sonic-perpetual-trading-ui-theta.vercel.app`
- **开发环境**：
  - 安装依赖：`npm install`
  - 启动开发服务：`npm run dev`

### 技术栈

- React + TypeScript
- React Router v7 应用路由
- Tailwind CSS
- Vite 构建

### 脚本说明

- `npm run dev`：本地开发（HMR）
- `npm run build`：构建生产版本
- `npm run start`：使用 `@react-router/serve` 启动构建后的 Node 服务器（本地/自托管场景）
- `npm run typecheck`：类型检查
- `npm run lint`：ESLint 检查

### CI / CD

- **GitHub Actions**
  - 工作流：`.github/workflows/ci.yml`
  - 在 `main` 分支的 `push` 和指向 `main` 的 `PR` 上运行：
    - `npm run typecheck`
    - `npm run lint`
    - `npm run build`
- **Vercel**
  - 连接 GitHub 仓库 `Erioser/SonicPerpetualTradingUI`
  - 每次推送自动构建并部署
  - PR 自动生成 Preview 环境
