CSS微小知识
------  
#### list-style 设置列表的属性  
在未加修饰的浏览器原生环境下，用`<ul>`标签写出一个ul列表的样子会是下面这样的  

* 1
* 2
* 3
* 4

css中的 `list-style` 可以来帮助我们改变赋予 `<ul>` 的原生样式，它的可选属性有三个  

`list-style-type` 设置列表每一项前标识符的类型，默认是原点`disc`，也可以设置方块或空心，具体值可查[W3C](http://www.w3school.com.cn/css/pr_list-style-type.asp)
```css
 list-style-type: none   /*去除标识*/
 list-style-type: circle   /*空心*/
 list-style-type: square   /*方块*/
```

`list-style-image` 用图像来替换列表项的标记  
```css
 list-style-image: url(http://img3.imgtn.bdimg.com/it/u=1672459557,2888362768&fm=26&gp=0.jpg)
```

`list-style-position` 设置列表项标记的位置，默认 `outside`
```css
 list-style-position: outside  /*标记在文本左侧，且位于文本外*/
 list-style-position: inside   /*标记位于文本以内*/
```

list-style可连用，比如：`list-style: square inside`
