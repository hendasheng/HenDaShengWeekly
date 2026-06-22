# WeChat Converter - AI 参考

## 核心原则

**复制到公众号的内容必须和预览完全一致。** 任何样式改动必须同时修改两处：

1. **`#preview` CSS 规则**（`<style>` 中）→ 控制预览显示
2. **`const STYLES` 对象**（`<script>` 中）→ 控制复制出去的内联样式

两处的属性值必须一一对应，否则预览和公众号效果不一致。

## 文件结构

```
tools/wechat-converter/
├── convert.html   ← 核心文件，单文件包含 HTML/CSS/JS
└── AGENTS.md      ← 本文件
```

页面通过 VS Code Live Server 打开，通过 `fetch` 探测 `../../docs/vol.xxx.md` 自动加载最新一期周刊。

## 关键函数

| 函数 | 作用 |
|---|---|
| `render()` | 解析 Markdown → 预览 DOM，会先去掉 `# 很大声周刊-vol.xxx` 行 |
| `buildStyledHTML()` | 克隆预览 DOM → 应用 STYLES 内联样式 → 返回 HTML 字符串 |
| `doCopy()` | 调 `buildStyledHTML()` 拿到带内联样式的 HTML，写入剪贴板 |
| `applyInlineStyles()` | (已废弃) 被 `buildStyledHTML` 内的 `walk()` 替代 |

## 样式对应关系

修改样式时，假设调整 `h1` 的 `font-size`：

- **预览 CSS**：`#preview h1 { font-size: 21px; ... }`
- **内联 STYLES**：`h1: 'font-size:21px;...'`

两处都要同步修改。CSS 属性名和值保持一致。

## 特殊处理

1. **去掉期号**：`render()` 用正则在解析前移除 `# 很大声周刊-vol.xxx`
2. **第一个 h1 无 margin-top**：预览用 `#preview h1:first-of-type`；复制在 `buildStyledHTML()` 中检测第一个 `h1` 替换 margin
3. **pre > code**：复制时会清除 code 的背景色，因 pre 已有深色背景
4. **h1-h4 内的 strong**：复制时会重置为继承色，避免双重强调

## 剪贴板机制

优先用 `navigator.clipboard.write()` 写入 `text/html` + `text/plain`。如失败（如非 HTTPS），降级为创建可见临时元素 → `execCommand('copy')` → 删除临时元素。
