# 常用js方法

#####1.获取字符串中 中文 和 数字的长度

``` javascript
var str = "中文，数字123456，world！";

console.log('中文长度：'+str.replace(/[^\u4e00-\u9fa5]/g,"").length); //将非中文替换空字符串，返回中文长度

console.log('数字长度：'+str.replace(/[^0-9]/g,"").length); //将非数字替换空字符串，返回数字长度
```
#####2.去除数组重复元素

``` javascript
//对象键值覆盖去重
var docker = ['aa','bb','cc','aa',11,22,33,11],
    result = {};
    
for(var i = 0;i < docker.length;i++){
    result[docker[i]] = docker[i]; //用元素作为键值。
}
for(var key in result){
   console.log(result[key]);
}
```

## scrollIntoView

DOM的滚动

DOM规范中并没有规定各浏览器需要实现怎样的滚动页面区域，各浏览器实现了相应的方法，可以使用不同的方式控制页面区域的滚动。这些方法作为HTMLElement类型的扩展存在，所以它能在所有元素上使用。

1、scrollIntoView(alignWithTop)  滚动浏览器窗口或容器元素，以便在当前视窗的可见范围看见当前元素。如果alignWithTop为true，或者省略它，窗口会尽可能滚动到自身顶部与元素顶部平齐。-------目前各浏览器均支持

2、scrollIntoViewIfNeeded(alignCenter) 只在当前元素在视窗的可见范围内不可见的情况下，才滚动浏览器窗口或容器元素，最终让当前元素可见。如果当前元素在视窗中可见，这个方法不做任何处理。如果将可选参数alignCenter设置为true，则表示尽量将元素显示在视窗中部（垂直方向）------Safari、Chrome实现了这个方法

3、scrollByLines(lineCount) 将元素的内容滚动指定的行数的高度，lineCount的值可以为正值或是负值。---Safari、Chrome实现了这个方法

4、scrollByPages(pageCount) 将元素的内容滚动指定的页面的高度，具体高度由元素的高度决定。---Safari、Chrome实现了这个方法

 

scrollIntoView()和scrollIntoVIewIfNeeded()作用的是元素的窗口，而scrollByLines()、scrollByPages()影响元素自身，下面是几个示例：

//将页面主体滚动5行

document.body.scrollByLines(5);

 

//确保当前元素可见

document.getElementById(“test”).scrollIntoView();   //

//true:对象的顶端与当前窗口的顶部对齐

//false:对象的底端与当前窗口的顶部对齐

 

//确保只在当前元素不可见的情况下才使其可见

document.getElementById(“test”).scrollIntoViewIfNeeded();

 

//将页面主体往回滚1页

doument.body.scrollByPages(-1);

由于只有scrollIntoView被各浏览器均支持，所以这个方法最为常用
