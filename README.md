# hello-wiki

基于 **pnpm** 的 monorepo，Web 应用使用 [Next.js](https://nextjs.org)（位于 `apps/web`），配套 React 19、TypeScript 与 Tailwind CSS v4。

## 本地开发

在仓库根目录执行：

| 命令 | 说明 |
|------|------|
| `pnpm dev` | 启动开发服务器（默认 <http://localhost:3000>） |
| `pnpm build` | 生产构建 |
| `pnpm start` | 启动生产服务（需先 build） |
| `pnpm lint` | 运行 ESLint |

页面入口：`apps/web/src/app/page.tsx`，修改后热更新。

## 项目结构

```
hello-wiki/
├── apps/
│   └── web/          # Next.js 应用
├── package.json      # 根脚本与 workspace
└── pnpm-lock.yaml
```

## 参考文档

- [Next.js 文档](https://nextjs.org/docs)
- [Next.js 部署说明](https://nextjs.org/docs/app/building-your-application/deploying)

## Git Commit 规范

提交信息建议使用类型前缀，便于检索与变更说明：

| 类型 | 说明 |
|------|------|
| **feat** | 新增 feature |
| **fix** | 修复 bug |
| **docs** | 仅仅修改了文档，比如 README、CHANGELOG、CONTRIBUTE 等等 |
| **style** | 仅仅修改了空格、格式缩进、逗号等等，不改变代码逻辑 |
| **refactor** | 代码重构，没有加新功能或者修复 bug |
| **perf** | 优化相关，比如提升性能、体验 |
| **test** | 测试用例，包括单元测试、集成测试等 |
| **chore** | 改变构建流程、或者增加依赖库、工具等 |
| **revert** | 回滚到上一个版本 |

示例：`feat: 添加词条搜索`、`fix: 修正目录跳转错误`。
