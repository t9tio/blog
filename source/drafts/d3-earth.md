---
title: 用 D3 画一个数据驱动的地球
date: 2019-08-01
---


## 画地球需要掌握的三个概念

在网页上画地球, 就是一个将而为球面上的坐标转换为平面上坐标的过程. 要进行这个转换我们需要掌握三个概念

- GeoJSON: JSON 格式的地理数据
- projections: 把经纬度转换为 x,y 坐标的函数(球面坐标转为平面坐标有很多不同的方法)
- path generators: 由 (GeoJSON, projections) 生成 SVG/Canvas path 的函数

Result
<p class="codepen" data-height="423" data-theme-id="dark" data-default-tab="result" data-user="timqian" data-slug-hash="dxWgBY" style="height: 423px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="d3-geo-basic">
  <span>See the Pen <a href="https://codepen.io/timqian/pen/dxWgBY/">
  d3-geo-basic</a> by 钱利江 (<a href="https://codepen.io/timqian">@timqian</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>