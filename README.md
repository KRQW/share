# 常用js方法

#####1.获取字符串中 中文 和 数字的长度

``` javascript
var str = "怎样从一个Html页面中提取所有汉字呢？不能有其它Html代码。数字123456";

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
