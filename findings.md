# 研究发现

## 技术决策
1. **TailwindCSS**: 使用 CDN 引入，`<script src="https://cdn.tailwindcss.com"></script>`，无需构建工具
2. **单文件架构**: 所有HTML/CSS/JS在一个 `index.html` 中，方便分发使用
3. **深色模式**: 使用 class 切换 + Tailwind `dark:` 前缀，存储在 localStorage

## 设计决策（通过 ui-ux-pro-max-skill 搜索确定）
1. **配色方案**: Primary #2563EB, Secondary #3B82F6, CTA #F97316, Background #F8FAFC(#0F172A dark), Text #1E293B
2. **设计风格**: Micro-interactions（微交互风格），圆角卡片，平滑过渡
3. **排版**: Inter 字体（Google Fonts CDN），清晰易读
4. **深色模式**: class 切换 + Tailwind `dark:` 前缀，存储在 localStorage
5. **反模式避免**: 无emoji图标（使用SVG），无不必要的动画，无过度设计

## 安全审查（纯前端，无安全风险）
- 无后端API，无数据传输
- 无硬编码密钥
- 所有数据存储在浏览器本地（localStorage）
- Notification API 需要用户显式授权

## API/库选择
- TailwindCSS: CDN play CDN
- 无其他依赖，纯原生实现

## 浏览器兼容性
- 现代浏览器（Chrome/Firefox/Edge/Safari）
- Notification API 需要用户授权
- AudioContext 用于提示音