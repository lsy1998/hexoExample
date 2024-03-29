---
create_date: '2023-06-24 17:14'
title: hsl()和hsla()
categories:
  - CSS
  - 知识点
---

## hsl()
**HSL** 即：**色相**（Hue）、**饱和度**（ Saturation ）、**亮度**（ Lightness ）。
> 色相（H）是色彩的基本属性，就是平常所说的颜色名称，如红色、黄色等。
> 饱和度（S）是指色彩的纯度，越高色彩越纯，低则逐渐变灰，取0 ~ 100%的数值。
> 亮度（L），取0 ~ 100%，增加亮度，颜色会向白色变化；减少亮度，颜色会像黑色变化。

|值	|描述|
|----|----|
|hue - 色相|定义色相（0到360）-0（或360）为红色，120为绿色，240为蓝色|
|saturation - 饱和度	|定义饱和度；0%为灰色，100%全白|
|lightness - 亮度	|定义亮度0%为暗，50%为普通，100%为白|
### 语法

```css
hsl(hue, saturation , lightness); 
```

## hsla()
**HSLA** 即：色相、饱和度、亮度、**透明度**（英语：Hue, Saturation , Lightness , Alpha ）。
> 透明度（A） 取值 0~1 之间， 代表透明度。
### 语法

```css
hsla(hue, saturation , lightness ,alpha)
```