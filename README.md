# FE_bugfix
######1.css cube引起cubepage上点击事件无法响应
```html
<div class="space3d">
    <div class="_3dbox">
      <div class="_3dface _3dface--front"></div>
      <div class="_3dface _3dface--top"></div>
      <div class="_3dface _3dface--bottom"></div>
      <div class="_3dface _3dface--left"></div>
      <div class="_3dface _3dface--right"></div>
      <div class="_3dface _3dface--back"></div>
    </div>
</div>
```
>div._3dface上的button,:hover...事件可能无法响应

解决办法：给div.space3d添加{perspective: 1000000px;}
