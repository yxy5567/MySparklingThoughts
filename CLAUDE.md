# CLAUDE.md

本仓库是个人 Markdown 文档库（人生感悟、职业思考、技术思考与笔记、问题解决记录），不是代码项目，没有构建和测试。Claude 的职责是文档归档与 git 管理，作者负责写内容。

## 目录与分类

- 按类别分多级目录，当前结构见 [README.md](README.md)。
- 新文档按内容归入最贴近的分类；没有合适的就新建子目录，并同步更新 README 的目录说明。
- 用户自己放进某个目录的文档，尊重其分类，不擅自移动。分类明显有误时先提出，再改。
- 图片等资源放 `_assets/`，文档中用相对路径引用。
- 目录里有真实文件后，删掉该目录的 `.gitkeep`。

## 命名

- 文件名：`YYYY-MM-DD-标题.md`。日期用文档入库当天，用户另有指定的除外。
- 标题取文档的主题，可以和正文一级标题不同；保留中文和全角标点。

## 处理新文档的流程

1. `git status --short --untracked-files=all` 找出新增或改动的文件。
2. 通读内容，确定分类和文件名。
3. 不改正文内容。错别字、格式问题只指出，经用户同意再改。
4. 提交并推送到 `origin main`。

## Git 约定

- 远端：https://github.com/yxy5567/MySparklingThoughts.git，分支 `main`，直接提交到 main。
- 提交信息用中文：`新增：<标题>`、`修改：<标题>`、`调整：<说明>`。
- 按路径暂存具体文件，不用 `git add .`。
- 已设置 `core.quotepath false`，中文路径显示正常；换行统一为 LF（见 `.gitattributes`）。
- 在 PowerShell 里，`git push` 的进度信息走 stderr，会显示成 NativeCommandError，这是正常现象，看到 `main -> main` 就说明推送成功。
