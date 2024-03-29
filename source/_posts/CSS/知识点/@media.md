---
create_date: '2023-06-24 17:14'
title: '@media'
categories:
  - CSS
  - 知识点
---

**@media** 规则在媒体查询中用于为不同的媒体类型/设备应用不同的样式。
媒体查询可用于检查许多事情，诸如：
> 视口的宽度和高度
> 设备的宽度和高度
> 方向（手机或平板电脑处于横屏还是竖屏模式？）
> 分辨率

## 媒体类型

| 值|描述|
|--|--|
|all|默认。用于所有媒体类型设备。|
|print|用于打印机。|
|screen|用于计算机屏幕、平板电脑、智能手机等。|
|speech|用于朗读页面的屏幕阅读器。|

## 媒体特性

|值|描述|
|--|--|
|any-hover|是否有任何可用的输入机制允许用户（将鼠标等）悬停在元素上？在 Media Queries Level 4 中被添加。|
|any-pointer|可用的输入机制中是否有任何指针设备，如果有，它的精度如何？在 Media Queries Level 4 中被添加。|
|aspect-ratio|视口（viewport）的宽高比。|
|color|输出设备每个像素的比特值，常见的有 8、16、32 位。如果设备不支持输出彩色，则该值为 0。|
|color-gamut|用户代理和输出设备大致程度上支持的色域。在 Media Queries Level 4 中被添加。|
|color-index|输出设备的颜色查询表（color lookup table）中的条目数量。如果设备不使用颜色查询表，则该值为 0。|
|device-aspect-ratio|输出设备的宽高比。已在 Media Queries Level 4 中被弃用。|
|device-height|输出设备渲染表面（如屏幕）的高度。已在 Media Queries Level 4 中被弃用。|
|device-width|输出设备渲染表面（如屏幕）的宽度。已在 Media Queries Level 4 中被弃用。|
|display-mode|应用程序的显示模式，如 web app 的 manifest 中的 display 成员所指定在 Web App Manifest spec 被定义。|
|forced-colors|检测是用户代理否限制调色板。在 Media Queries Level 5 中被添加。|
|grid|输出设备使用网格屏幕还是点阵屏幕？|
|height|视口（viewport）的高度。|
|hover|主输入机制是否允许用户将鼠标悬停在元素上？在 Media Queries Level 4 中被添加。|
|inverted-colors|浏览器或者底层操作系统是否反转了颜色。在 Media Queries Level 5 中被添加。|
|light-level|当前环境光水平。在 Media Queries Level 5 中被添加。|
|max-aspect-ratio|显示区域的宽度和高度之间的最大比例。|
|max-color|输出设备每个颜色分量的最大位数。|
|max-color-index|设备可以显示的最大颜色数。|
|max-height|显示区域的最大高度，例如浏览器窗口。|
|max-monochrome|单色（灰度）设备上每种“颜色”的最大位数。|
|max-resolution|设备的最大分辨率，使用 dpi 或 dpcm。|
|max-width|显示区域的最大宽度，例如浏览器窗口。|
|min-aspect-ratio|显示区域的宽度和高度之间的最小比例。|
|min-color|输出设备每个颜色分量的最小位数。|
|min-color-index|设备可以显示的最小颜色数。|
|min-height|显示区域的最小高度，例如浏览器窗口。|
|min-monochrome|单色（灰度）设备上每种“颜色”的最小位数。|
|min-resolution|设备的最低分辨率，使用 dpi 或 dpcm。|
|min-width|显示区域的最小宽度，例如浏览器窗口。|
|monochrome|输出设备单色帧缓冲区中每个像素的位深度。如果设备并非黑白屏幕，则该值为 0。|
|orientation|视窗（viewport）的旋转方向（横屏还是竖屏模式）。|
|overflow-block|输出设备如何处理沿块轴溢出视口(viewport)的内容。在 Media Queries Level 4 中被添加。|
|overflow-inline|沿内联轴溢出视口(viewport)的内容是否可以滚动？在 Media Queries Level 4 中被添加。|
|pointer|主要输入机制是一个指针设备吗？如果是，它的精度如何？在 Media Queries Level 4 中被添加。|
|prefers-color-scheme|探测用户倾向于选择亮色还是暗色的配色方案。在 Media Queries Level 5 中被添加。|
|prefers-contrast|探测用户是否有向系统要求提高或降低相近颜色之间的对比度。在 Media Queries Level 5 中被添加。|
|prefers-reduced-motion|用户是否希望页面上出现更少的动态效果。在 Media Queries Level 5 中被添加。|
|prefers-reduced-transparency|用户是否倾向于选择更低的透明度。在 Media Queries Level 5 中被添加。|
|resolution|输出设备的分辨率，使用 dpi 或 dpcm。|
|scan|输出设备的扫描过程（适用于电视等）。|
|scripting|探测脚本（例如 JavaScript）是否可用。在 Media Queries Level 5 中被添加。|
|update|输出设备更新内容的渲染结果的频率。在 Media Queries Level 4 中被添加。|
|width|视窗（viewport）的宽度。|
## not、only 和 and 关键字的含义：
1. **not**：not 关键字反正整个媒体查询的含义。
2. **only**：only 关键字可防止旧版浏览器应用指定的样式，这些浏览器不支持带媒体特性的媒体查询。它对现代浏览器没有影响。
3. **and**：and 关键字将媒体特性与媒体类型或其他媒体特性组合在一起。

它们都是可选的。但是，如果使用 not 或 only，则还必须指定媒体类型。

您还可以针对不同的媒体使用不同的样式表，就像这样：
```html
<link rel="stylesheet" media="screen and (min-width: 900px)" href="widescreen.css">
<link rel="stylesheet" media="screen and (max-width: 600px)" href="smallscreen.css">
```

## 例子
### 例子1
```css
@media screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
```