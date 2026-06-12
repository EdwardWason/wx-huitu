# 设计令牌参考

> CSS变量体系 + 双风格主题 + 字号规范
> 版本: 1.0 | 画布: 横版 640×auto / 方版 640×640

---

## 1. CSS变量体系

### 通用变量（所有图表共享）

```css
:root {
  /* 基础色 */
  --ink: #0a0a0a;
  --paper: #fafaf8;
  --accent: #002FA7;
  --muted: #737373;
  --rule: #d4d4d2;

  /* 字体 */
  --font-body: 'Noto Sans SC', sans-serif;

  /* 图表色板 (Okabe-Ito 色盲安全) */
  --chart-1: #E69F00;
  --chart-2: #56B4E9;
  --chart-3: #009E73;
  --chart-4: #D55E00;
  --chart-5: #CC79A7;
  --chart-6: #F0E442;
  --chart-7: #0072B2;
  --chart-8: #000000;
}
```

### 主题切换

只替换 `:root` 变量即可切换主题：

**克制风（默认）**
```css
:root { --accent: #002FA7; }
```

**品牌DNA — 微信绿**
```css
:root { --accent: #07C160; }
```

**品牌DNA — 经济学人红**
```css
:root { --accent: #E3120B; }
```

**品牌DNA — 知乎蓝**
```css
:root { --accent: #0066FF; }
```

**暖色系**
```css
:root { --accent: #C0392B; --paper: #f8f6f1; }
```

---

## 2. 字号规范

### 图表专用字号

| 元素 | 字号 | 字重 | 颜色 | 用途 |
|------|------|------|------|------|
| kicker | 11px | 500 | --accent | 分类标签 |
| title | 20-24px | 500 | --ink | 图表标题 |
| axis-label | 11-12px | 400 | --muted | 轴刻度标签 |
| data-label | 12-13px | 500 | --ink / --paper | 数据标注 |
| legend-text | 12-13px | 400 | --ink | 图例文字 |
| source | 11px | 400 | --muted | 数据来源 |
| num-mega | 48-64px | 200 | --ink | billboard大数字 |
| num-label | 14-16px | 500 | --accent | billboard标签 |

### 标题长度→字号映射

| 标题长度 | 字号 | 字重 |
|---------|------|------|
| ≤6字 | 24px | 500 |
| 7-14字 | 22px | 500 |
| 15-24字 | 18px | 500 |
| 25+字 | 16px | 500 |

---

## 3. 间距规范

| 元素 | 间距 |
|------|------|
| 页面内边距 | 40-48px |
| 标题与图表间距 | 20-28px |
| 图表行间距 | 10-14px |
| 图例项间距 | 16-20px |
| 来源与图表间距 | 16-20px |

---

## 4. 图表尺寸规范

| 格式 | 宽度 | 高度 | 比例 |
|------|------|------|------|
| 横版 | 640px | auto (400-800px) | flexible |
| 方版 | 640px | 640px | 1:1 |

### 高度参考

| 图型 | 建议高度 |
|------|---------|
| bar-chart (4条) | ~500px |
| bar-chart (8条) | ~700px |
| h-bar-chart (8条) | ~600px |
| line-chart | ~500px |
| flow-chart (5步) | ~550px |
| layered-diagram (4层) | ~500px |
| waterfall-chart (6项) | ~500px |
