# pixelMAP

这是一个基于 Mapbox GL JS，用来记录我和朋友们去了哪里旅行的像素小人旅行地图:)
你可以把左侧角色拖拽到地图任意位置，记录地点名称、旅行日期和一句备注，并在本地持久化保存。

## 功能特点

- 像素角色拖拽上图并生成标记
- 地点搜索（Mapbox Geocoder）
- 标记信息录入：地点名、日期、备注
- 标记编辑、删除、整图清空
- 标记可二次拖动调整坐标
- 基于 `localStorage` 的本地数据持久化

## 项目结构

```text
pixelMAP/
├─ Explorebymap.html   # 主页面（结构 + 交互逻辑）
├─ map.css             # 页面样式
├─ assets/             # 角色图片素材（可替换成你自己的角色）
└─ IowanOldStyleBT-*.otf  # 自定义字体
```

## 自定义角色素材

- `assets/` 目录中的角色图片可以按需替换为你自己的 PNG 素材。
- 在 `Explorebymap.html` 里新增/修改对应的 `.character-item`，让 `data-character` 与图片文件名保持一致。
- 示例：`data-character="myrole"` 对应图片 `assets/myrole.png`。

## 快速开始

1. 克隆或下载项目到本地。
2. 直接用浏览器打开 `Explorebymap.html`。
3. 左侧选择角色并拖到地图上，填写旅行信息后保存。

## 数据存储

- 本地存储键名：`pixelMapMarkers`
- 存储位置：浏览器 `localStorage`
- 清除方式：点击页面左侧“清空地图”按钮

## 注意事项

- 项目依赖外部 CDN（Mapbox GL JS / Geocoder），离线环境无法正常加载地图。
- 请确认 Mapbox Token 可用且有对应样式访问权限。
- 若页面中文出现乱码，请确认文件编码为 UTF-8。

## 后续可扩展方向

- 导出/导入旅行数据（JSON）
- 多地图主题切换
- 标记筛选（按人名、日期）
- 云端同步与多人协作
