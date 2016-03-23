# html常用方法

##### 修改css3伪类值
``` html
<!-- html -->
<a href="" data-val="555" class="upd-val"></a>
```
```css
/** css **/
.upd-val:after{
  content:attr(data-val);
}
```
