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
div._3dface上的button,:hover...事件可能无法响应

解决办法：给div.space3d添加{perspective: 1000000px;}

#######2./\s/.test(str) 相当于 str.search(/\s/),只有返回值不同

#######3.中文chrome最小字号12px
解决办法：-webkit-text-size-adjust:none，缺陷：页面缩放是这些文字不会变化，因此尽量设为局部属性

但是该属性在chrome27后无效，替代方案，transfrom:scale(0.8)
