一个为 Discourse 论坛添加圣诞节装饰效果的主题组件。

## 🎄 项目概述

- **项目名称**: discourse-christmas-decorations
- **类型**: Discourse 主题组件 (Theme Component)
- **作者**: Meghna
- **许可证**: MIT License
- **功能**: 为 Discourse 论坛添加圣诞节装饰效果

## 📁 项目结构

```
discourse-christmas-decorations/
├── about.json          # 组件元数据配置
├── settings.yml        # 用户可配置的设置
├── LICENSE             # MIT 许可证
├── README.md           # 项目说明
├── assets/             # 静态资源
│   ├── hat.png         # 圣诞帽图片
│   ├── christmas-decoration.png  # 圣诞装饰图片
│   └── hat.png.bak     # 备份文件
├── common/             # 通用文件
│   ├── after_header.html  # 页面头部后的HTML模板
│   └── common.scss     # 主样式文件
└── scss/               # 样式模块
    ├── variables.scss  # 变量和函数
    ├── lights.scss     # 圣诞灯效果
    ├── hats.scss       # 圣诞帽效果
    └── image.scss      # 装饰图片效果
```

## ⚙️ 功能特性

### 1. 圣诞灯效果 (`lights.scss`)
- 创建动态闪烁的圣诞灯串
- 使用 CSS 动画实现不同颜色的灯光闪烁
- 支持绿色、蓝色、青色三种颜色
- 响应式设计，移动端适配

### 2. 圣诞帽装饰 (`hats.scss`)
- 为用户头像添加圣诞帽
- 支持多种变换效果（旋转、翻转、缩放）
- 应用于：
  - 话题页面头像
  - 话题列表最新回复者头像
  - 当前用户头像
  - 最新话题列表项

### 3. 装饰图片 (`image.scss`)
- 在大屏幕设备上显示圣诞装饰图片
- 支持颜色反转（适配深色主题）
- 仅在屏幕宽度 ≥ 1450px 时显示

## 🎛️ 可配置选项

通过 `settings.yml` 文件可以配置以下选项：

1. **enable_lights**: 启用/禁用圣诞灯效果
2. **enable_hats**: 显示/隐藏头像圣诞帽
3. **enable_decoration_image**: 显示/隐藏装饰图片
4. **decoration_invert_color**: 装饰图片颜色反转（适配深色主题）

## 🛠️ 技术实现

### HTML 结构
- 使用 `<ul class="lightrope">` 创建圣诞灯串
- 通过 40 个 `<li>` 元素实现灯光效果

### CSS 技术
- **SCSS 预处理器**: 使用变量、函数、条件编译
- **CSS 动画**: 关键帧动画实现闪烁效果
- **伪元素**: `::after` 和 `::before` 创建装饰效果
- **响应式设计**: 媒体查询适配不同屏幕尺寸

### 资源管理
- 图片资源通过 `about.json` 中的 `assets` 字段管理
- 支持主题设置的条件渲染

## 🌟 项目亮点

1. **模块化设计**: 功能分离，易于维护
2. **高度可配置**: 用户可自定义各种装饰效果
3. **性能优化**: 使用 CSS 动画而非 JavaScript
4. **响应式**: 适配桌面和移动设备
5. **主题兼容**: 支持深色主题的颜色反转

## 📝 使用场景

这个组件适用于：
- Discourse 论坛的圣诞节主题装饰
- 社区节庆氛围营造
- 用户体验增强
- 节日营销活动

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🔗 相关链接

- [Discourse 主题组件文档](https://meta.discourse.org/t/christmas-decoration-component/173949)
- [GitHub 仓库](https://github.com/MeghnaAJ/discourse-christmas-decorations)
