# AGENTS.md

## 仓库性质

- 这是 GitHub 个人主页仓库（`zhuchentong/zhuchentong`）：根目录的 `README.md` 会直接渲染在 GitHub 个人主页上。
- 仓库只有 `README.md`，没有代码、构建、测试、lint 或 CI。不要寻找或创建 package.json、工作流等文件。
- 默认分支为 `master`，远程为 SSH（`git@github.com:zhuchentong/zhuchentong.git`）。

## 编辑 README.md 的注意事项

- 对 `README.md` 的修改在 push 后会立即公开显示在用户的 GitHub 主页，属于用户可见的公众内容；未经明确要求不要 commit / push。
- 正文风格为英文简介 + 中文个人名（紫菜苔 / zhuchentong），修改时保持现有风格。
- 技能图标使用 `raw.githubusercontent.com/github/explore/...` 的固定 commit 链接，防止上游变动导致图标失效；不要随意“升级”这些 URL。
- `github-readme-stats.vercel.app` 的统计图为远程动态生成，无法在本地验证渲染结果，检查改动时不要依赖它。
