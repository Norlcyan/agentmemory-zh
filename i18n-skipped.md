# i18n 未译清单

> 文件：`src/viewer/index.html`（agentmemory Web Viewer 简体中文汉化）
> 原则：只替换“用户可见的英文字符串字面量”。以下字符串因会改动逻辑、标识符或无法确认仅用于显示，**故意保留英文**。

## 分类统计

| 类别 | 记录数 | 去重字符串数 |
|---|---|---|
| 枚举值/状态值/程序键 | 410 | 173 |
| 标识符/变量名/函数名 | 470 | 295 |
| 元素 id/选择器 | 195 | 94 |
| CSS 类名 | 202 | 108 |
| data-* 属性键 | 54 | 45 |
| JSON 键名/字段名 | 92 | 42 |
| URL/API 路径 | 138 | 90 |
| 命令/MCP/示例/环境变量 | 57 | 41 |
| HTML 标记片段 | 1057 | 464 |
| HTML 属性值（非显示） | 28 | 11 |
| 拿不准（人工复核后未译） | 40 | 37 |
| 其他 | 295 | 182 |

## 各类别说明与示例

### 枚举值/状态值/程序键

被代码比较或用作程序键的字符串——翻译会破坏逻辑，**必须保持英文**。共 410 条记录，去重 173 个不同字符串。

代表性示例（`en` → 未译原因）：

- `<li><span class="badge badge-muted">rule</span>` — uncertain: 徽章类别标签（rule），是否为数据枚举拿不准
- `<li><span class="badge badge-red">error</span>` — uncertain: 徽章类别标签（error），是否为数据枚举拿不准
- `A sentinel fired` — 审计操作类型（数据枚举）
- `Added core memory` — 审计操作类型（数据枚举）
- `Appended to a slot` — 审计操作类型（数据枚举）
- `ArrowLeft` — 键盘事件 key 值（代码）
- `ArrowRight` — 键盘事件 key 值（代码）
- `BUTTON` — 标签名比较（代码）
- `Compacted graph provenance` — 审计操作类型（数据枚举）
- `Compressed observations` — 审计操作类型（数据枚举）
- `Created a sentinel` — 审计操作类型（数据枚举）
- `Created a slot` — 审计操作类型（数据枚举）
- ……（另有 161 个，完整记录见 `.i18n-work/skipped-*.json`）

### 标识符/变量名/函数名

变量名、函数名、对象键等标识符。共 470 条记录，去重 295 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` active` — 代码标识符或标点片段，非用户可见文本
- ` checked` — 代码标识符或标点片段，非用户可见文本
- ` current` — 代码标识符或标点片段，非用户可见文本
- ` disabled` — 代码标识符或标点片段，非用户可见文本
- ` disabled title="No session has a` — uncertain: 该 title 由三段拼接（含维度代码变量 project/agent/status），无法逐段译成通顺中文
- ` fresh` — CSS 类名/变量/媒体查询/选择器/元素 id：CSS 类名片段
- ` off` — 代码标识符或标点片段，非用户可见文本
- ` on` — 代码标识符或标点片段，非用户可见文本
- ` selected` — 代码标识符或标点片段，非用户可见文本
- ` yet"` — uncertain: 该 title 由三段拼接（含维度代码变量），无法逐段译成通顺中文
- `" aria-current="` — 选择器/URL/API 路径/查询参数/代码标识符，非用户可见文本
- `" aria-label="` — 选择器/URL/API 路径/查询参数/代码标识符，非用户可见文本
- ……（另有 283 个，完整记录见 `.i18n-work/skipped-*.json`）

### 元素 id/选择器

getElementById / querySelector / CSS 引用的元素 id。共 195 条记录，去重 94 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` disabled title="No memory has a` — uncertain: 碎片化拼接（'No memory has a' + 'n agent id'/' '+dim + ' yet'），逐片
- `#action-detail` — 元素 id
- `#health-` — 元素 id 前缀
- `#lesson-detail` — 元素 id
- `#ses-head` — DOM 选择器（代码）
- `#session-detail` — 元素 id
- `#session-list` — DOM 选择器（代码）
- `#view-` — 元素 id 前缀
- `-filter` — 元素 id 片段（代码）
- `<div class="audit-more" id="audit-detail-` — HTML 标记/id 前缀
- `[data-action="close-modal"]` — DOM 选择器（代码）
- `[data-action="ses-confirm-summarize"]` — DOM 选择器（代码）
- ……（另有 82 个，完整记录见 `.i18n-work/skipped-*.json`）

### CSS 类名

样式表引用的类名。共 202 条记录，去重 108 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` active` — CSS 类名（代码）
- ` bad` — CSS 类名（代码）
- ` btn-primary` — CSS 类名（代码）
- ` compact` — CSS 类名（代码）
- ` err` — CSS 类名
- ` focus` — CSS 类名（代码）
- ` fresh` — CSS 类名（代码）
- ` mid` — CSS 类名（代码）
- ` offline` — CSS 类名
- ` ok` — CSS 类名
- ` on` — CSS 类名（代码）
- ` open` — CSS 类名（条件拼接）
- ……（另有 96 个，完整记录见 `.i18n-work/skipped-*.json`）

### data-* 属性键

data-* 属性的键名。共 54 条记录，去重 45 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` data-action="goto-tab" data-tab="` — data-* 属性/role 属性值/aria 属性值
- `" aria-hidden="true">` — data-* 属性/role 属性值/aria 属性值：aria 属性值
- `" data-action-id="` — data-* 属性名（代码）
- `" data-audit-row="` — data-* 属性键
- `" data-crystal-id="` — data-* 属性键
- `" data-obs-id="` — data-* 属性名（代码）
- `" role="link" tabindex="0"` — data-* 属性/role 属性值/aria 属性值：role 属性值
- `action-clear-filters` — 动作名（data-action 对比值）
- `action-close` — 动作名（data-action 对比值）
- `action-set-status` — 动作名（data-action 对比值）
- `activity-clear` — 动作名（data-action 对比值）
- `activity-day` — 动作名（data-action 对比值）
- ……（另有 33 个，完整记录见 `.i18n-work/skipped-*.json`）

### JSON 键名/字段名

API/存储的 JSON 字段名。共 92 条记录，去重 42 个不同字符串。

代表性示例（`en` → 未译原因）：

- `ArrowDown` — 键盘键名（代码）
- `ArrowLeft` — 键盘键名（代码）
- `ArrowRight` — 键盘键名（代码）
- `ArrowUp` — 键盘键名（代码）
- `Escape` — 键盘键名（代码）
- `What the agent learned in this session` — 命令示例中的示例内容（curl 示例的 content 字段值）
- `action` — entityList('action') 的实体键名（代码）
- `agentId` — facet 维度键名（代码）
- `agentmemory-theme` — localStorage 键名（代码）
- `agentmemory-viewer-token` — localStorage 键名（代码）
- `agents` — facet 维度键名（代码）
- `command` — JSON 键名（代码）
- ……（另有 30 个，完整记录见 `.i18n-work/skipped-*.json`）

### URL/API 路径

URL、API 路径、路由。共 138 条记录，去重 90 个不同字符串。

代表性示例（`en` → 未译原因）：

- `#dashboard` — 链接 href（代码）
- `&agentId=` — API 查询参数（代码）
- `&body=` — URL 查询参数（保留不译）
- `&cursor=` — API 查询参数（代码）
- `&dateFrom=` — URL 查询串
- `&dateTo=` — URL 查询串
- `&limit=` — API 查询参数（代码）
- `&limit=20` — API 查询参数（代码）
- `&limit=50` — API 查询参数（代码）
- `&minImportance=` — API 查询参数（代码）
- `&operation=` — URL 查询串
- `&project=` — API 查询参数（代码）
- ……（另有 78 个，完整记录见 `.i18n-work/skipped-*.json`）

### 命令/MCP/示例/环境变量

shell 命令、MCP 工具名与示例、环境变量名、示例数据。共 57 条记录，去重 41 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` --port ` — 命令行命令/参数/示例命令中的占位值：命令行参数片段
- ` \\\n  -H 'Content-Type: application/json' \\\n  -d '` — 终端/curl 命令（代码，保留原文）
- `/path/to/project` — 命令行命令/参数/示例命令中的占位值：示例命令中的占位参数值
- `CI failed twice on type errors` — 命令示例中的示例内容
- `Checkout totals apply coupons first` — 示例命令中的示例值（用户需替换为自己的值，不翻译）
- `Coupons apply before shipping thresholds` — 代码示例中的示例数据（保留原文）
- `README.md` — 命令示例中的文件名
- `Run tsc before committing` — 命令示例中的示例内容
- `Ship v1` — 命令示例中的示例内容
- `The API uses jose for JWT validation` — 命令行命令/参数/示例命令中的占位值：示例命令中的示例内容值，翻译会改变命令语义
- `Use named CSS grid areas in checkout` — 示例命令中的示例值（用户需替换为自己的值，不翻译）
- `architecture` — 命令行命令/参数/示例命令中的占位值：示例命令中的参数值
- ……（另有 29 个，完整记录见 `.i18n-work/skipped-*.json`）

### HTML 标记片段

HTML 标签/属性片段（非自然语言）。共 1057 条记录，去重 464 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` &rarr;</a>` — HTML 实体与标记片段（无自然语言）
- ` <button type="button" class="linkish" data-action="activity-day" data-day="` — HTML 标签/属性片段，非用户可见文本
- ` <button type="button" class="linkish" data-action="mem-diff" data-memory-id="` — HTML 标签/属性片段，非用户可见文本
- ` <code style="font-size:10px;color:var(--ink-faint);font-weight:400;">` — HTML 标记片段（无自然语言）
- ` <span class="badge ` — HTML 标记片段
- ` <span class="ready-badge" title="` — HTML 结构片段，无显示文本
- ` <span style="color:var(--ink-faint);">(` — HTML 标签/属性片段，非用户可见文本
- ` <span style="color:var(--ink-muted);">(` — HTML 标记片段
- ` <span>` — HTML 结构片段，无显示文本
- ` disabled` — HTML 属性名/属性值（代码）
- ` ms</td></tr>` — HTML 结构片段（含计量单位 ms，中文保持不变）
- ` open` — HTML 属性名/属性值（代码）
- ……（另有 452 个，完整记录见 `.i18n-work/skipped-*.json`）

### HTML 属性值（非显示）

meta 等非显示属性值。共 28 条记录，去重 11 个不同字符串。

代表性示例（`en` → 未译原因）：

- `_blank` — 链接 target 属性值（代码）
- `checkbox` — input type 属性值（代码）
- `dialog` — ARIA role 属性值（代码）
- `noopener` — 链接 rel 属性值（代码）
- `presentation` — ARIA role 属性值（代码）
- `status` — ARIA role 属性值（代码）
- `tablist` — ARIA role 属性值（代码）
- `tabpanel` — ARIA role 属性值（代码）
- `tooltip` — ARIA role 属性值（代码）
- `viewport` — meta 标签 name 属性值（代码，非显示文本）
- `width=device-width, initial-scale=1.0` — meta 标签 content 属性值（代码）

### 拿不准（人工复核后未译）

人工复核后仍无法确认只用于显示的字符串。共 40 条记录，去重 37 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` added, &minus;` — uncertain: 复数后缀 's' 未纳入候选，整句 '+N word(s) added, −M removed' 无法逐片完整翻译
- ` bucket` — uncertain: 与未收录的复数后缀 's' 拼接（p.buckets===1?'':'s'），单独翻译会破坏语义
- ` crystal` — uncertain: 与未收录的复数后缀 's' 拼接（items.length===1?'':'s'），单独翻译会渲染为“5 结晶s”，需
- ` earlier version` — uncertain: 复数后缀 's' 未纳入候选，逐片翻译会导致“X 个更早版本s”
- ` matching entr` — uncertain: 与未收录的复数后缀 'y'/'ies' 拼接（rows.length===1?'y':'ies'），单独翻译会渲染为“
- ` matching memor` — uncertain: 后缀 'y'/'ies' 未纳入候选（'matching memory'/'matching memories'），无
- ` memor` — uncertain: 后缀 'y'/'ies' 未纳入候选，无法完整翻译
- ` minute` — uncertain: 与未收录的复数后缀 's' 拼接（mins===1?'':'s'），单独翻译会渲染为“90 分钟s”，需先处理复数逻辑
- ` observation` — uncertain: 复数后缀 's' 未纳入候选，逐片翻译会导致混杂
- ` of type <b>` — uncertain: 与 ' observation' 碎片联动，整句无法逐片完整翻译
- ` older version` — uncertain: 复数后缀 's'（older.length===1?'':'s'）未纳入候选，逐片翻译会导致“X 个旧版本s”
- ` permanently?</h3>` — uncertain: 后缀 'y'/'ies' 未纳入候选，无法完整翻译
- ……（另有 25 个，完整记录见 `.i18n-work/skipped-*.json`）

### 其他

路由标识、switch case、kind 标识等程序逻辑值。共 295 条记录，去重 182 个不同字符串。

代表性示例（`en` → 未译原因）：

- ` &times;` — 符号（计数分隔符 ×），无需翻译
- ` KiB` — 单位符号，保留原文
- ` MB` — 计量单位，中文保持不变
- ` feature` — 复数拼接逻辑：代码按数量追加 's'，直接翻译片段会残留 's'
- ` fill="` — SVG 结构片段
- ` non-2xx body was not JSON:` — console 日志（非用户可见）
- ` off` — 复数拼接的片段（feature/features/off），单独翻译会破坏 chip 文本
- ` returned ` — console 日志（非用户可见）
- ` session` — 复数拼接逻辑：代码按数量追加 's'，直接翻译片段会残留 's'（如“会话s”）
- ` stroke-dasharray="` — SVG 结构片段
- ` · active ` — 与复数逻辑/timeAgo 绑定的选项文本片段，单独翻译会产生中英混杂
- `" cy="` — SVG 结构片段
- ……（另有 170 个，完整记录见 `.i18n-work/skipped-*.json`）

## 特别说明

1. **复数后缀中和**：英文单复数三元表达式 `(n === 1 ? '' : 's')` 在中文下被替换为空字符串 `''`（共约 30 处），这是汉化所必需的显示调整，不属于逻辑变更；相关候选在初审时标为“不确定”，已逐行人工解决，不在此清单中重复列出。
2. **审计操作动词（AUDIT_VERBS）**：初审时因形似枚举而跳过；经核查其值仅用于显示（`auditVerb(op)` 查询、无任何值比较、过滤器使用键），已全部翻译。
3. **审计操作过滤器**下拉框显示的是操作键原文（如 `lesson_save`），因改动渲染取值属于逻辑变更，按“只换字符串”原则保留原样。
4. **时间表达**：`timeAgo`/`durationText` 等函数内的英文时间单位已随所在区段翻译；`relTime` 输出的相对时间保持原实现。
5. `setWsStatus(text, cls)` 的 CSS 类参数（如 `connecting`）保留英文，仅翻译显示文本参数；静态 HTML 中 `ws-status` 的 `connecting` 类曾被误改，已恢复。