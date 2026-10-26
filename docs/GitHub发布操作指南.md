# GitHub 发布操作指南（Mac 新手版）

推荐用 GitHub Desktop 图形界面，第一版不用敲 Git 命令。

## 第 1 步：准备公开仓库文件

1. 下载项目的 GitHub Starter ZIP 并解压。
2. 打开解压后的 `wechat-moments-polisher` 文件夹。
3. 检查 `references/` 里只有模板，没有你的私人朋友圈、私人飞书地址或访问凭据。
4. README、SKILL.md、LICENSE、docs、examples 和 dist 应该都在项目文件夹中。

## 第 2 步：安装 GitHub Desktop

1. 打开 https://desktop.github.com/ 下载 macOS 版。
2. 安装并启动。
3. 登录你的 GitHub 账号。

## 第 3 步：创建本地仓库

1. 在 GitHub Desktop 菜单选择 `File` → `New repository...`。
2. Name 填 `wechat-moments-polisher`。
3. Local path 选一个容易找到的位置，例如 `Documents/GitHub`。
4. 如果有 `Initialize this repository with a README` 选项，可以勾选。
5. 点击 `Create repository`。

## 第 4 步：把项目文件放进仓库

1. 在 GitHub Desktop 里点击 `Show in Finder`，打开刚创建的本地仓库目录。
2. 把第 1 步解压出来的项目文件夹里的**所有内容**复制到这个仓库目录。注意是里面的内容，不要再套一层同名文件夹。
3. 如果系统询问是否替换 README，请用本项目提供的 README 替换。
4. 回到 GitHub Desktop，左侧应出现一批新增或修改的文件。
5. 检查列表中没有私人配置文件后再继续。

## 第 5 步：提交并发布到 GitHub

1. 在窗口左下角的 `Summary` 填：`Initial release: WeChat Moments Polisher Skill`。
2. 点击 `Commit to main`。
3. 点击顶部的 `Publish repository`。
4. Repository name 使用 `wechat-moments-polisher`；选择 **Public**，不要选 Private。
5. 确认发布。
6. 发布后点击 `View on GitHub`，检查网页能看到 README 和文件目录。

## 第 6 步：完善仓库主页

1. README 第一屏要有一句话介绍、真实演示 GIF 或案例、安装步骤。
2. 在仓库右侧 `About` 的齿轮按钮里填写 Description，并添加 Topics：`agent-skills`、`wechat`、`ai-writing`、`content-creation`、`workbuddy`（仅保留确实适用的主题）。
3. 检查仓库是否包含 LICENSE。MIT 适合希望别人自由使用、修改和再分发的项目；如不希望别人这样使用，先选择与你的目标一致的许可证。
4. 先用 WorkBuddy 或你最熟悉的 Agent 实测安装，再在 README 标记测试情况。没有测试的兼容性，不要写成“已验证”。

## 第 7 步：固定到个人主页

1. 在 GitHub 右上角头像菜单中点 `Your profile`。
2. 在 `Pinned` 区域点击 `Customize your pins`。
3. 选择 `wechat-moments-polisher` 并保存。
4. 项目成熟后，再考虑制作个人 Profile README：新建一个与 GitHub 用户名完全相同的公开仓库，并在根目录放 `README.md`。

## 第 8 步：发布后分享

使用仓库真实地址替换下方占位符：

> 我把自己日常使用的朋友圈文案方法整理成了一个中文 Agent Skill，开源了。
>
> 它不是帮你批量生成营销文案，而是结合个人背景和最多 20 条历史朋友圈，把图片、草稿或零散想法整理成更像本人表达的内容。默认保留原意，不编造经历，也不为了显得深刻硬拔高。
>
> 目前先支持我实际测试过的 Agent，欢迎试用、提 Issue，也欢迎告诉我哪些地方写得不像真人。
>
> GitHub：`[替换成仓库真实地址]`

不要承诺 Star 数，也不要写未经验证的效果数据。优先展示真实的输入、原始输出、限制和迭代记录。
