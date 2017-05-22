# -Cascading-Style-Sheet-
日常CSS样式


### 计算滚动条宽度
``` css
.wrap-outer {
    padding-left: calc(100vw - 100%);
}

```
参考链接: http://www.zhangxinxu.com/wordpress/2015/01/css-page-scrollbar-toggle-center-no-jumping/

### 响应式布局
** /屏幕大于等于1921,/ **
```
@media screen and (min-width: 1921px){
    
}


@media screen and (max-width: 1920px) and (min-width: 1780px) {

}


@media screen and (max-width: 1779px) and (min-width: 1440px) {


}

@media screen and (max-width: 1439px) and (min-width: 1366px) {


}

@media screen and (max-width: 1365px) and (min-width: 1080px) {

    
}

@media screen and (max-width: 1079px) {


}
```
---

### CSS 文本超出?行就隐藏并且显示省略号
```
Element{
    overflow:hidden;  //超出隐藏
    text-overflow:ellipsis; //溢出用省略号显示
    display:-webkit-box; //将对象作为弹性伸缩盒子模型显示。
    -webkit-box-orient:vertical; //从上到下垂直排列子元素（设置伸缩盒子的子元素排列方式）
    -webkit-line-clamp:2; //这个属性不是css的规范属性，需要组合上面两个属性，表示显示的行数
}
```

### CSS实现滚动条出现页面不跳动
```
html {
  overflow-y: scroll;
}

:root {
  overflow-y: auto;
  overflow-x: hidden;
}

:root body {
  position: absolute;
}

body {
  width: 100vw;
  overflow: hidden;
}
```

### CSS判断手机横屏竖屏
```
@media all and (orientation : landscape) { 

    /*横屏时...*/

} 

@media all and (orientation : portrait){ 

    /*竖屏时...*/

} 
```

### 模糊元素(滤镜, 高斯, 毛玻璃)
```
存在较大兼容问题:(主要是IE10,IE11,以及firefox)
	.box_filter {
    -webkit-filter: blur(3px); /* Chrome, Opera */
       -moz-filter: blur(3px);
        -ms-filter: blur(3px);    
            filter: blur(3px);   
    filter: progid:DXImageTransform.Microsoft.Blur(PixelRadius=3, MakeShadow=false); /* IE6 IE9 */
	}
    
参考:
	http://www.zhangxinxu.com/wordpress/2013/11/css-svg-image-blur/
 ```
    
    
    
### 黑白照片:
```
.gray {
    -webkit-filter: grayscale(100%);
    -moz-filter: grayscale(100%);
    -ms-filter: grayscale(100%);
    -o-filter: grayscale(100%);
    filter: grayscale(100%);
    filter: gray;
}
```


### input 表单清除默认样式
```
input:-webkit-autofill {
    -webkit-box-shadow: 0 0 0 1000px white inset;
}
```

### 文本底对齐
```
    vertical-align: middle;
    或者
    vertical-align: -webkit-baseline-middle;
```
