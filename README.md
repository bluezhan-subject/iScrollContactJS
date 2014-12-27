iScrollContactJS
================

一个Javascript库, 允许您创建一个类似通讯录首字母滑动的效果 
用法
-----------------------------------  
内容页面的目标元素(elements:#ID)调用iScroll( )方法
它创造了必要的HTML元素在内容页面
右边操作元素(elements:#ID)调用iScrollContact( )方法
使用HTML 5新标签和CSS 3最新标准

引用库
```javascript
require.config({
  baseUrl: "js/",
  paths: {
    "jquery": "libs/jquery203",
    "iScroll": "libs/iScroll425",
    "iScrollContact": "iScrollContact"
  },
  /*iScrollContact.js符合AMD规范，才可以调用*/
  shim: {
    'iScroll': {
      exports: 'iScroll'
    },
    'iScrollContact': {
      deps: ['iScroll'],
      exports: 'iScrollContact'
    }
  }
});
```


HTML
```html
<!-- dom elements -->
<ul id="abc-tab3"></ul>

<div id="roll-tips-tab3">
<p id="roll-tips-tab3-p"></p>
</div>

<div id="wrapper-tab3"></div>
```


.sticker {
width: 180px;
height: 180px;
}

// add image
.example-1 .sticker-img {
background-image: url(heroes-2.png);
}
CSS
```css
// add color
.example-2 .sticker-img {
background-color: #ff4a85;
}

// change shadow opacity
.example-2 .sticker-shadow {
opacity: 0.6;
}
```
使用

```js
window.scrollTo(0,0);

//完全消除myscroll及其占用的内存空间
// myscroll.destroy()
myScrollTab3 = new iScroll('wrapper-tab3');
myScrollContactTab3 = new iScroll_Contact_Fn('scroller-tab3');
new abc('abc-tab3',myScrollTab3,myScrollContactTab3,'roll-tips-tab3');
````







