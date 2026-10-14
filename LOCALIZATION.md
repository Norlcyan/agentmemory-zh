# 汉化说明（agentmemory-zh）

本仓库是 [rohitg00/agentmemory](https://github.com/rohitg00/agentmemory) 的**非官方简体中文汉化 fork**，遵循上游的 Apache-2.0 许可证。

## 汉化范围

- **仅**汉化 Web Viewer 界面：`src/viewer/index.html` 中用户可见的字符串（导航、标题、按钮、提示、空状态、术语表等）。
- 代码逻辑、标识符、枚举值、程序键（`data-tab`、过滤器键等）、CLI 文案均保持上游原样；上游已知的 bug 不在本 fork 的修改范围内。
- 英文的单复数后缀机制（如 `1 session` / `2 sessions` 的 `s`）在中文下中和为空，不影响任何其他行为。

## 基线与对照

- 基于上游 commit：`36eb328`（2026-10-13）。
- 全部译文对照见 `i18n-mapping.json`（1470 条）；有意未译的字符串及原因见 `i18n-skipped.md`。

## 同步上游的方法

```bash
git fetch upstream
git merge upstream/main
# 如 viewer 有新增字符串，参照 i18n-mapping.json 的术语表补译
```

## 术语表（节选）

Overview=总览，Memories=记忆，Observations=观测，Sessions=会话，Lessons=经验教训，Crystals=结晶，Graph=图谱，Consolidation=整合，Context injection=上下文注入，Health=健康状态，Audit=审计，Replay=回放，Actions=行动，Profile=档案，Live feed=实时动态，Knowledge graph=知识图谱。

## 验收修复记录（首版）

首版汉化经独立复核后修复了以下问题（均在 commit 历史中可查）：

1. 两处 JS 模板字符串里的 HTML 包装结构被误删，已恢复：加载骨架屏的 `<div class="skeleton">`、授权提示的 `<div class="viewer-auth-title">`（仅译其中文本）。
2. `copyBtn` 的按钮文本译为「复制」后，全站 25 处 `.replace('>copy<', …)` 按钮改名逻辑同步迁移为 `.replace('>复制<', …)`，确保改名逻辑与按钮实际文本一致、行为与上游等价。
