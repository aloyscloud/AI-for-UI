# 将本工具包加入你的 GitHub 仓库

目标仓库：<https://github.com/aloyscloud/AI-for-UI>

## 方案 A：网页端上传（适合第一次操作）

1. 下载并解压 `AI_UI_Design_Lab_Starter.zip`。
2. 打开你的仓库，在 GitHub 页面进入 `Add file` → `Upload files`。
3. 将解压后的文件夹内内容拖入页面。若浏览器不保留空目录，没关系；这些目录都有文件。
4. 不要直接覆盖现有 README 前，先保存原 README 内容。推荐用工具包中的 README 作为新结构，再把原本说明并入顶部的项目简介。
5. 在页面底部填写提交说明：`docs: add AI UI design workflow and prompt templates`。
6. 推荐先提交到新分支 `docs/ai-ui-workflow`，然后创建 Pull Request 检查差异；确认无误后再合并到 `main`。

## 方案 B：Git 命令行（推荐，便于以后迭代）

```bash
git clone https://github.com/aloyscloud/AI-for-UI.git
cd AI-for-UI

git checkout -b docs/ai-ui-workflow
```

把工具包里的文件和目录复制到仓库根目录。**先备份并比较现有 README，不要未经检查直接覆盖。** 然后运行：

```bash
git status --short
git diff -- README.md
# 检查新增文件是否包含密钥、个人信息或不应公开的原文内容

git add README.md SOURCES.md docs prompts skills experiments GITHUB_STEPS.md
git diff --cached --stat
git diff --cached
```

若差异确认无误：

```bash
git commit -m "docs: add AI UI design workflow and prompt templates"
git push -u origin docs/ai-ui-workflow
```

随后在 GitHub 上创建 Pull Request，检查内容后合并。

## 上传前必查

- `SOURCES.md` 的来源链接是否准确。
- 没有把不可见/付费文章内容写成逐字翻译。
- 没有复制未获许可的第三方 Skill 文件。
- 没有 API key、token、`.env` 或隐私数据。
- 所有尚未运行的实验都标记为待验证。

## 重要说明

这些步骤只指导你把文件提交到自己的仓库；除非你本人完成并确认 GitHub 提交，否则不要在 README 中声称本工具包已经被推送或通过端到端测试。
