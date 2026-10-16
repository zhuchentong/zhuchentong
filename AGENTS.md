# AGENTS.md

## 仓库性质

- 这是 GitHub 个人主页仓库（`zhuchentong/zhuchentong`）：根目录的 `README.md` 会直接渲染在 GitHub 个人主页上。
- 仓库无代码、构建、测试或 lint；CI 是两个 workflow：`.github/workflows/snake.yml`（贡献贪吃蛇）和 `.github/workflows/wakatime.yml`（WakaTime 周统计），见下文。
- 默认分支为 `master`，远程为 SSH（`git@github.com:zhuchentong/zhuchentong.git`）。
- `assets/` 下有两个自绘 SVG：`cyber-terminal.svg`（SMIL 打字动画）和 `neon-divider.svg`（静态霓虹分割线）。SMIL 动画在 GitHub README 的 `<img>` 中可用；修改后须在浏览器中本地验证再提交。

## 编辑 README.md 的注意事项

- 对 `README.md` 的修改在 push 后会立即公开显示在用户的 GitHub 主页，属于用户可见的公众内容；未经明确要求不要 commit / push。
- 正文风格为英文简介 + 中文个人名（紫菜苔 / zhuchentong），修改时保持现有风格。
- 技能图标墙使用 `skillicons.dev`（深色卡片自带霓虹感）；不要再使用已废弃的 shields.io 技能徽章或 `raw.githubusercontent.com/github/explore` 图标链接。
- `github-readme-stats.vercel.app` 的统计图为远程动态生成，无法在本地验证渲染结果，检查改动时不要依赖它。
- 贪吃蛇动画由 `.github/workflows/snake.yml` 生成：每日 UTC 16:00 及 push 到 master 时运行 `Platane/snk/svg-only@v3`，产物推送到 `output` 分支（该分支由 Action 管理，勿手动修改）。README 通过 `raw.githubusercontent.com/zhuchentong/zhuchentong/output/...` 引用。首次或改动后可在 Actions 页面手动 `workflow_dispatch` 触发一次验证。
- WakaTime 统计由 `.github/workflows/wakatime.yml` 生成：每 6 小时 UTC 及手动 `workflow_dispatch` 运行 `anmol098/waka-readme-stats@master`，结果写入 README 中 `<!--START_SECTION:waka-->` / `<!--END_SECTION:waka-->` 标记对之间（This Week I Spent My Time On + AI Coding This Week），Action 用 PAT 直接 commit 到 master。依赖仓库 secrets `WAKATIME_API_KEY`（wakatime.com API key）与 `GH_TOKEN`（classic PAT，repo scope）。本地编辑 README 时不要增删标记对内部的 Action 生成内容。
