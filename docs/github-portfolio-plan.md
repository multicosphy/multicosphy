# GitHub 仓库组织方案

目标是把 GitHub 账号整理成三个清晰板块：个人兴趣、课程作业项目、研究与论文探索。

## 1. 仓库分组方式

GitHub 个人账号下没有真正的文件夹分组，建议用以下组合来实现分类：

- 仓库命名：用统一前缀区分类型。
- Topics：给仓库加标签，便于筛选。
- `Cosphy` README：在 `multicosphy/Cosphy` 仓库首页做总索引。
- Pinned repositories：把最能代表当前阶段的 4-6 个仓库固定在主页。

## 2. 命名规范

建议仓库名以英文为主，并采用首字母大写的类型前缀。GitHub 页面上会保留大小写展示，但 URL 与部分 Git 操作通常不应依赖大小写区分，因此不要同时创建只差大小写的仓库名。

中文或中英混合仓库名在 GitHub 上通常可以创建，但不建议作为长期主仓库命名：URL、命令行、自动化脚本、包管理工具、引用链接和跨平台路径处理更容易出现编码或可读性问题。更稳妥的做法是仓库名用英文，README 标题和描述使用中文。

### 个人兴趣

适合放长期兴趣、阅读笔记、工具实验和非课程性质的积累。

- `Interest-*`
- `Notes-*`
- `Reading-*`

建议 Topics：

- `personal-interest`
- `reading-notes`
- `finance`
- `ai`

### 课程作业项目

适合放课程材料、作业代码、报告和复现实验。

- `Course-*`
- `Course-YYYY-topic`

示例：

- `Course-financial-time-series-analysis`

建议 Topics：

- `coursework`
- `financial-time-series`
- `econometrics`
- `python`
- `private-study`

### 研究与论文探索

适合放从课程或兴趣中沉淀出的独立问题、可复现实验、论文草稿和研究笔记。

- `Research-*`
- `Paper-*`
- `Project-*`

示例：

- `Research-shibor-forecasting`
- `Paper-time-series-foundation-models`
- `Project-financial-forecasting-lab`

建议 Topics：

- `research`
- `paper-draft`
- `time-series`
- `forecasting`
- `reproducible-research`

## 3. 当前课程仓库

当前仓库 `multicosphy/Course-financial-time-series-analysis` 承载《金融时间序列分析》课程内容。

建议：

1. 保持仓库为 private，除非确认课程课件、论文 PDF 和作业报告可以公开。
2. 保留当前目录结构，不把课件、参考论文和作业代码拆到同一个扁平目录。
3. 视频文件继续放在 Git 外部，因为普通 GitHub 仓库不适合保存 223MB 的 mp4。
4. 本地远端地址保持为：

```bash
git remote set-url origin https://github.com/multicosphy/Course-financial-time-series-analysis.git
```

## 4. 后续 Codex 维护规则

以后创建或更新 GitHub 项目时，Codex 应同时处理以下事项：

1. 按仓库用途选择命名前缀：`Course-*`、`Research-*`、`Paper-*`、`Project-*`、`Notes-*`、`Reading-*` 或 `Interest-*`。
2. 创建或更新 `README.md`，写清项目目标、目录结构、数据来源、运行方法和版本管理说明。
3. 自动维护 Topics；新建仓库时设置初始 Topics，后续项目定位变化时同步更新。
4. 大文件不直接进入普通 Git 仓库，优先使用网盘、Release 或 Git LFS。
5. 课程仓库可以完整保存过程材料；研究仓库只保留可复现的核心材料。

## 5. 常用 Topics

课程类：

- `coursework`
- `private-study`
- `lecture-notes`
- `assignment`

研究类：

- `research`
- `paper-draft`
- `reproducible-research`
- `time-series`
- `forecasting`

兴趣与笔记类：

- `personal-interest`
- `reading-notes`
- `knowledge-base`
- `finance`
- `ai`

总索引类：

- `portfolio`
- `repository-index`
- `github-profile`
