
## 常用主流移动设备CSS3 Media Queries整理

使用的时候根据实际的需要进行条件判断，其中 
`landscape` 表示设备 `横屏` 情况 ，`portrait` 表示设备 `竖屏` 情况

`max-device-width` 表示设备最大分辨率宽度，`min-device-width` 表示设备最小分辨率宽度

关于 `min-width` 和 `min-device-width` 的区别是，前者是指的网页窗口的最小宽度，后者是指设备最小分辨率宽度，同理 `max-width` 和 `max-device-width`，前者是指网页窗口的最大宽度，后者是指设备最大分辨率宽度。

值得注意的是 我们在写设备页面适配的时候，不要忘记加上这句，要不然页面在PC端模拟测试是没有效果的。

``` html

<meta name="viewport" content="width=device-width,user-scalable=no" />

```

意思是：设置屏幕宽度为设备宽度，禁止用户手动调整缩放，关于viewpotr其他具体参数设置，可以百度查阅。

``` css

@charset "utf-8";

/**
 * iPhone 4/4s landscape & portrait
 */
@media only screen
and (min-device-width: 320px)
and (max-device-width: 480px) {

}

/**
 * iPhone 4/4s portrait
 */
@media only screen
and (min-device-width: 320px)
and (max-device-width: 480px)
and (orientation:portrait)  {

}

/**
 * iPhone 4/4s landscape
 */
@media only screen
and (min-device-width: 320px)
and (max-device-width: 480px)
and (orientation:landscape) {

}

/**
 *  iPhone 5/5s landscape & portrait
 */
@media only screen
and (min-device-width: 320px)
and (max-device-width: 568px) {

}

/**
 *  iPhone 5/5s portrait
 */
@media only screen
and (min-device-width: 320px)
and (max-device-width: 568px)
and (orientation: portrait) {

}

/**
 *  iPhone 5/5s landscape
 */
@media only screen
and (min-device-width: 320px)
and (max-device-width: 568px)
and (orientation: landscape) {

}

/**
 *  iPhone 6 landscape & Portrait
 */
@media only screen 
and (min-device-width: 375px) 
and (max-device-width: 667px) {

}

/**
 *  iPhone 6  Portrait
 */
@media only screen 
and (min-device-width: 375px) 
and (max-device-width: 667px) 
and (orientation : portrait) { 

}

/**
 *  iPhone 6  landscape
 */
@media only screen 
and (min-device-width: 375px) 
and (max-device-width: 667px) 
and (orientation : landscape) { 

}

/**
 *  iPhone 6+  Portrait
 */
@media only screen 
and (min-device-width: 414px) 
and (max-device-width: 736px) 
and (orientation : portrait) { 

}

/**
 *  iPhone 6+  landscape
 */
@media only screen 
and (min-device-width: 414px) 
and (max-device-width: 736px) 
and (orientation : landscape) { 

}

/**
 *  Galaxy S3 landscape & portrait
 */
@media screen
and (device-width: 320px)
and (device-height: 640px) {

}

/**
 *  Galaxy S3 portrait
 */
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (orientation: portrait) {

}

/**
 *  Galaxy S3 landscape
 */
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (orientation: landscape) {

}

/**
 *  Galaxy S5 landscape & portrait
 */
@media screen
and (device-width: 360px)
and (device-height: 640px) {

}

/**
 *  Galaxy S5 portrait
 */
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (orientation: portrait) {

}

/**
 *  Galaxy S5 landscape
 */
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (orientation: landscape) {

}

/**
 *  iPad  landscape & portrait
 */
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (-webkit-min-device-pixel-ratio: 1) {

}

/**
 *  iPad  portrait
 */
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: portrait)
and (-webkit-min-device-pixel-ratio: 1) {

}

/**
 *  iPad  landscape
 */
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: landscape)
and (-webkit-min-device-pixel-ratio: 1) {

}

```

## box loading
``` css
/*-- Created in shadowPainter : ) */
.box {
position: absolute;
top: 0px;
bottom: 0px;
left: 0px;
right: 0px;
margin: auto;
width: 119px;
height: 119px;
overflow: hidden;
border: 1px solid #DDD;
}
.dot {
display: block;
position: absolute;
width: 17px;
height: 17px;
top: -17px;
left: -17px;
-webkit-animation: 2s shadows linear infinite;
animation: 2s shadows linear infinite;
box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #FF3D7F, 17px 34px 0 0 #FF9E9D, 17px 51px 0 0 #DAD8A7, 17px 68px 0 0 #7FC7AF, 17px 85px 0 0 #3FB8AF, 17px 102px 0 0 #FF3D7F, 17px 119px 0 0 #FF9E9D, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #3FB8AF, 34px 34px 0 0 #FF3D7F, 34px 51px 0 0 #FF9E9D, 34px 68px 0 0 #DAD8A7, 34px 85px 0 0 #7FC7AF, 34px 102px 0 0 #3FB8AF, 34px 119px 0 0 #FF3D7F, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #7FC7AF, 51px 34px 0 0 #3FB8AF, 51px 51px 0 0 #FF3D7F, 51px 68px 0 0 #FF9E9D, 51px 85px 0 0 #DAD8A7, 51px 102px 0 0 #7FC7AF, 51px 119px 0 0 #3FB8AF, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #DAD8A7, 68px 34px 0 0 #7FC7AF, 68px 51px 0 0 #3FB8AF, 68px 68px 0 0 #FF3D7F, 68px 85px 0 0 #FF9E9D, 68px 102px 0 0 #DAD8A7, 68px 119px 0 0 #7FC7AF, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #FF9E9D, 85px 34px 0 0 #DAD8A7, 85px 51px 0 0 #7FC7AF, 85px 68px 0 0 #3FB8AF, 85px 85px 0 0 #FF3D7F, 85px 102px 0 0 #FF9E9D, 85px 119px 0 0 #DAD8A7, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #FF3D7F, 102px 34px 0 0 #FF9E9D, 102px 51px 0 0 #DAD8A7, 102px 68px 0 0 #7FC7AF, 102px 85px 0 0 #3FB8AF, 102px 102px 0 0 #FF3D7F, 102px 119px 0 0 #FF9E9D, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #3FB8AF, 119px 34px 0 0 #FF3D7F, 119px 51px 0 0 #FF9E9D, 119px 68px 0 0 #DAD8A7, 119px 85px 0 0 #7FC7AF, 119px 102px 0 0 #3FB8AF, 119px 119px 0 0 #FF3D7F;
}

/* Keyframes */

@-webkit-keyframes shadows {
0% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #FF3D7F, 17px 34px 0 0 #FF9E9D, 17px 51px 0 0 #DAD8A7, 17px 68px 0 0 #7FC7AF, 17px 85px 0 0 #3FB8AF, 17px 102px 0 0 #FF3D7F, 17px 119px 0 0 #FF9E9D, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #3FB8AF, 34px 34px 0 0 #FF3D7F, 34px 51px 0 0 #FF9E9D, 34px 68px 0 0 #DAD8A7, 34px 85px 0 0 #7FC7AF, 34px 102px 0 0 #3FB8AF, 34px 119px 0 0 #FF3D7F, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #7FC7AF, 51px 34px 0 0 #3FB8AF, 51px 51px 0 0 #FF3D7F, 51px 68px 0 0 #FF9E9D, 51px 85px 0 0 #DAD8A7, 51px 102px 0 0 #7FC7AF, 51px 119px 0 0 #3FB8AF, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #DAD8A7, 68px 34px 0 0 #7FC7AF, 68px 51px 0 0 #3FB8AF, 68px 68px 0 0 #FF3D7F, 68px 85px 0 0 #FF9E9D, 68px 102px 0 0 #DAD8A7, 68px 119px 0 0 #7FC7AF, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #FF9E9D, 85px 34px 0 0 #DAD8A7, 85px 51px 0 0 #7FC7AF, 85px 68px 0 0 #3FB8AF, 85px 85px 0 0 #FF3D7F, 85px 102px 0 0 #FF9E9D, 85px 119px 0 0 #DAD8A7, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #FF3D7F, 102px 34px 0 0 #FF9E9D, 102px 51px 0 0 #DAD8A7, 102px 68px 0 0 #7FC7AF, 102px 85px 0 0 #3FB8AF, 102px 102px 0 0 #FF3D7F, 102px 119px 0 0 #FF9E9D, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #3FB8AF, 119px 34px 0 0 #FF3D7F, 119px 51px 0 0 #FF9E9D, 119px 68px 0 0 #DAD8A7, 119px 85px 0 0 #7FC7AF, 119px 102px 0 0 #3FB8AF, 119px 119px 0 0 #FF3D7F;}
20% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #3FB8AF, 17px 34px 0 0 #FF3D7F, 17px 51px 0 0 #FF9E9D, 17px 68px 0 0 #DAD8A7, 17px 85px 0 0 #7FC7AF, 17px 102px 0 0 #3FB8AF, 17px 119px 0 0 #FF3D7F, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #7FC7AF, 34px 34px 0 0 #3FB8AF, 34px 51px 0 0 #FF3D7F, 34px 68px 0 0 #FF9E9D, 34px 85px 0 0 #DAD8A7, 34px 102px 0 0 #7FC7AF, 34px 119px 0 0 #3FB8AF, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #DAD8A7, 51px 34px 0 0 #7FC7AF, 51px 51px 0 0 #3FB8AF, 51px 68px 0 0 #FF3D7F, 51px 85px 0 0 #FF9E9D, 51px 102px 0 0 #DAD8A7, 51px 119px 0 0 #7FC7AF, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #FF9E9D, 68px 34px 0 0 #DAD8A7, 68px 51px 0 0 #7FC7AF, 68px 68px 0 0 #3FB8AF, 68px 85px 0 0 #FF3D7F, 68px 102px 0 0 #FF9E9D, 68px 119px 0 0 #DAD8A7, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #FF3D7F, 85px 34px 0 0 #FF9E9D, 85px 51px 0 0 #DAD8A7, 85px 68px 0 0 #7FC7AF, 85px 85px 0 0 #3FB8AF, 85px 102px 0 0 #FF3D7F, 85px 119px 0 0 #FF9E9D, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #3FB8AF, 102px 34px 0 0 #FF3D7F, 102px 51px 0 0 #FF9E9D, 102px 68px 0 0 #DAD8A7, 102px 85px 0 0 #7FC7AF, 102px 102px 0 0 #3FB8AF, 102px 119px 0 0 #FF3D7F, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #7FC7AF, 119px 34px 0 0 #3FB8AF, 119px 51px 0 0 #FF3D7F, 119px 68px 0 0 #FF9E9D, 119px 85px 0 0 #DAD8A7, 119px 102px 0 0 #7FC7AF, 119px 119px 0 0 #3FB8AF;}
40% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #7FC7AF, 17px 34px 0 0 #3FB8AF, 17px 51px 0 0 #FF3D7F, 17px 68px 0 0 #FF9E9D, 17px 85px 0 0 #DAD8A7, 17px 102px 0 0 #7FC7AF, 17px 119px 0 0 #3FB8AF, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #DAD8A7, 34px 34px 0 0 #7FC7AF, 34px 51px 0 0 #3FB8AF, 34px 68px 0 0 #FF3D7F, 34px 85px 0 0 #FF9E9D, 34px 102px 0 0 #DAD8A7, 34px 119px 0 0 #7FC7AF, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #FF9E9D, 51px 34px 0 0 #DAD8A7, 51px 51px 0 0 #7FC7AF, 51px 68px 0 0 #3FB8AF, 51px 85px 0 0 #FF3D7F, 51px 102px 0 0 #FF9E9D, 51px 119px 0 0 #DAD8A7, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #FF3D7F, 68px 34px 0 0 #FF9E9D, 68px 51px 0 0 #DAD8A7, 68px 68px 0 0 #7FC7AF, 68px 85px 0 0 #3FB8AF, 68px 102px 0 0 #FF3D7F, 68px 119px 0 0 #FF9E9D, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #3FB8AF, 85px 34px 0 0 #FF3D7F, 85px 51px 0 0 #FF9E9D, 85px 68px 0 0 #DAD8A7, 85px 85px 0 0 #7FC7AF, 85px 102px 0 0 #3FB8AF, 85px 119px 0 0 #FF3D7F, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #7FC7AF, 102px 34px 0 0 #3FB8AF, 102px 51px 0 0 #FF3D7F, 102px 68px 0 0 #FF9E9D, 102px 85px 0 0 #DAD8A7, 102px 102px 0 0 #7FC7AF, 102px 119px 0 0 #3FB8AF, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #DAD8A7, 119px 34px 0 0 #7FC7AF, 119px 51px 0 0 #3FB8AF, 119px 68px 0 0 #FF3D7F, 119px 85px 0 0 #FF9E9D, 119px 102px 0 0 #DAD8A7, 119px 119px 0 0 #7FC7AF;}
60% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #DAD8A7, 17px 34px 0 0 #7FC7AF, 17px 51px 0 0 #3FB8AF, 17px 68px 0 0 #FF3D7F, 17px 85px 0 0 #FF9E9D, 17px 102px 0 0 #DAD8A7, 17px 119px 0 0 #7FC7AF, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #FF9E9D, 34px 34px 0 0 #DAD8A7, 34px 51px 0 0 #7FC7AF, 34px 68px 0 0 #3FB8AF, 34px 85px 0 0 #FF3D7F, 34px 102px 0 0 #FF9E9D, 34px 119px 0 0 #DAD8A7, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #FF3D7F, 51px 34px 0 0 #FF9E9D, 51px 51px 0 0 #DAD8A7, 51px 68px 0 0 #7FC7AF, 51px 85px 0 0 #3FB8AF, 51px 102px 0 0 #FF3D7F, 51px 119px 0 0 #FF9E9D, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #3FB8AF, 68px 34px 0 0 #FF3D7F, 68px 51px 0 0 #FF9E9D, 68px 68px 0 0 #DAD8A7, 68px 85px 0 0 #7FC7AF, 68px 102px 0 0 #3FB8AF, 68px 119px 0 0 #FF3D7F, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #7FC7AF, 85px 34px 0 0 #3FB8AF, 85px 51px 0 0 #FF3D7F, 85px 68px 0 0 #FF9E9D, 85px 85px 0 0 #DAD8A7, 85px 102px 0 0 #7FC7AF, 85px 119px 0 0 #3FB8AF, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #DAD8A7, 102px 34px 0 0 #7FC7AF, 102px 51px 0 0 #3FB8AF, 102px 68px 0 0 #FF3D7F, 102px 85px 0 0 #FF9E9D, 102px 102px 0 0 #DAD8A7, 102px 119px 0 0 #7FC7AF, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #FF9E9D, 119px 34px 0 0 #DAD8A7, 119px 51px 0 0 #7FC7AF, 119px 68px 0 0 #3FB8AF, 119px 85px 0 0 #FF3D7F, 119px 102px 0 0 #FF9E9D, 119px 119px 0 0 #DAD8A7;}
80% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #FF9E9D, 17px 34px 0 0 #DAD8A7, 17px 51px 0 0 #7FC7AF, 17px 68px 0 0 #3FB8AF, 17px 85px 0 0 #FF3D7F, 17px 102px 0 0 #FF9E9D, 17px 119px 0 0 #DAD8A7, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #FF3D7F, 34px 34px 0 0 #FF9E9D, 34px 51px 0 0 #DAD8A7, 34px 68px 0 0 #7FC7AF, 34px 85px 0 0 #3FB8AF, 34px 102px 0 0 #FF3D7F, 34px 119px 0 0 #FF9E9D, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #3FB8AF, 51px 34px 0 0 #FF3D7F, 51px 51px 0 0 #FF9E9D, 51px 68px 0 0 #DAD8A7, 51px 85px 0 0 #7FC7AF, 51px 102px 0 0 #3FB8AF, 51px 119px 0 0 #FF3D7F, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #7FC7AF, 68px 34px 0 0 #3FB8AF, 68px 51px 0 0 #FF3D7F, 68px 68px 0 0 #FF9E9D, 68px 85px 0 0 #DAD8A7, 68px 102px 0 0 #7FC7AF, 68px 119px 0 0 #3FB8AF, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #DAD8A7, 85px 34px 0 0 #7FC7AF, 85px 51px 0 0 #3FB8AF, 85px 68px 0 0 #FF3D7F, 85px 85px 0 0 #FF9E9D, 85px 102px 0 0 #DAD8A7, 85px 119px 0 0 #7FC7AF, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #FF9E9D, 102px 34px 0 0 #DAD8A7, 102px 51px 0 0 #7FC7AF, 102px 68px 0 0 #3FB8AF, 102px 85px 0 0 #FF3D7F, 102px 102px 0 0 #FF9E9D, 102px 119px 0 0 #DAD8A7, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #FF3D7F, 119px 34px 0 0 #FF9E9D, 119px 51px 0 0 #DAD8A7, 119px 68px 0 0 #7FC7AF, 119px 85px 0 0 #3FB8AF, 119px 102px 0 0 #FF3D7F, 119px 119px 0 0 #FF9E9D;}

}
@keyframes shadows {
0% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #FF3D7F, 17px 34px 0 0 #FF9E9D, 17px 51px 0 0 #DAD8A7, 17px 68px 0 0 #7FC7AF, 17px 85px 0 0 #3FB8AF, 17px 102px 0 0 #FF3D7F, 17px 119px 0 0 #FF9E9D, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #3FB8AF, 34px 34px 0 0 #FF3D7F, 34px 51px 0 0 #FF9E9D, 34px 68px 0 0 #DAD8A7, 34px 85px 0 0 #7FC7AF, 34px 102px 0 0 #3FB8AF, 34px 119px 0 0 #FF3D7F, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #7FC7AF, 51px 34px 0 0 #3FB8AF, 51px 51px 0 0 #FF3D7F, 51px 68px 0 0 #FF9E9D, 51px 85px 0 0 #DAD8A7, 51px 102px 0 0 #7FC7AF, 51px 119px 0 0 #3FB8AF, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #DAD8A7, 68px 34px 0 0 #7FC7AF, 68px 51px 0 0 #3FB8AF, 68px 68px 0 0 #FF3D7F, 68px 85px 0 0 #FF9E9D, 68px 102px 0 0 #DAD8A7, 68px 119px 0 0 #7FC7AF, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #FF9E9D, 85px 34px 0 0 #DAD8A7, 85px 51px 0 0 #7FC7AF, 85px 68px 0 0 #3FB8AF, 85px 85px 0 0 #FF3D7F, 85px 102px 0 0 #FF9E9D, 85px 119px 0 0 #DAD8A7, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #FF3D7F, 102px 34px 0 0 #FF9E9D, 102px 51px 0 0 #DAD8A7, 102px 68px 0 0 #7FC7AF, 102px 85px 0 0 #3FB8AF, 102px 102px 0 0 #FF3D7F, 102px 119px 0 0 #FF9E9D, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #3FB8AF, 119px 34px 0 0 #FF3D7F, 119px 51px 0 0 #FF9E9D, 119px 68px 0 0 #DAD8A7, 119px 85px 0 0 #7FC7AF, 119px 102px 0 0 #3FB8AF, 119px 119px 0 0 #FF3D7F;}
20% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #3FB8AF, 17px 34px 0 0 #FF3D7F, 17px 51px 0 0 #FF9E9D, 17px 68px 0 0 #DAD8A7, 17px 85px 0 0 #7FC7AF, 17px 102px 0 0 #3FB8AF, 17px 119px 0 0 #FF3D7F, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #7FC7AF, 34px 34px 0 0 #3FB8AF, 34px 51px 0 0 #FF3D7F, 34px 68px 0 0 #FF9E9D, 34px 85px 0 0 #DAD8A7, 34px 102px 0 0 #7FC7AF, 34px 119px 0 0 #3FB8AF, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #DAD8A7, 51px 34px 0 0 #7FC7AF, 51px 51px 0 0 #3FB8AF, 51px 68px 0 0 #FF3D7F, 51px 85px 0 0 #FF9E9D, 51px 102px 0 0 #DAD8A7, 51px 119px 0 0 #7FC7AF, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #FF9E9D, 68px 34px 0 0 #DAD8A7, 68px 51px 0 0 #7FC7AF, 68px 68px 0 0 #3FB8AF, 68px 85px 0 0 #FF3D7F, 68px 102px 0 0 #FF9E9D, 68px 119px 0 0 #DAD8A7, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #FF3D7F, 85px 34px 0 0 #FF9E9D, 85px 51px 0 0 #DAD8A7, 85px 68px 0 0 #7FC7AF, 85px 85px 0 0 #3FB8AF, 85px 102px 0 0 #FF3D7F, 85px 119px 0 0 #FF9E9D, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #3FB8AF, 102px 34px 0 0 #FF3D7F, 102px 51px 0 0 #FF9E9D, 102px 68px 0 0 #DAD8A7, 102px 85px 0 0 #7FC7AF, 102px 102px 0 0 #3FB8AF, 102px 119px 0 0 #FF3D7F, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #7FC7AF, 119px 34px 0 0 #3FB8AF, 119px 51px 0 0 #FF3D7F, 119px 68px 0 0 #FF9E9D, 119px 85px 0 0 #DAD8A7, 119px 102px 0 0 #7FC7AF, 119px 119px 0 0 #3FB8AF;}
40% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #7FC7AF, 17px 34px 0 0 #3FB8AF, 17px 51px 0 0 #FF3D7F, 17px 68px 0 0 #FF9E9D, 17px 85px 0 0 #DAD8A7, 17px 102px 0 0 #7FC7AF, 17px 119px 0 0 #3FB8AF, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #DAD8A7, 34px 34px 0 0 #7FC7AF, 34px 51px 0 0 #3FB8AF, 34px 68px 0 0 #FF3D7F, 34px 85px 0 0 #FF9E9D, 34px 102px 0 0 #DAD8A7, 34px 119px 0 0 #7FC7AF, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #FF9E9D, 51px 34px 0 0 #DAD8A7, 51px 51px 0 0 #7FC7AF, 51px 68px 0 0 #3FB8AF, 51px 85px 0 0 #FF3D7F, 51px 102px 0 0 #FF9E9D, 51px 119px 0 0 #DAD8A7, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #FF3D7F, 68px 34px 0 0 #FF9E9D, 68px 51px 0 0 #DAD8A7, 68px 68px 0 0 #7FC7AF, 68px 85px 0 0 #3FB8AF, 68px 102px 0 0 #FF3D7F, 68px 119px 0 0 #FF9E9D, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #3FB8AF, 85px 34px 0 0 #FF3D7F, 85px 51px 0 0 #FF9E9D, 85px 68px 0 0 #DAD8A7, 85px 85px 0 0 #7FC7AF, 85px 102px 0 0 #3FB8AF, 85px 119px 0 0 #FF3D7F, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #7FC7AF, 102px 34px 0 0 #3FB8AF, 102px 51px 0 0 #FF3D7F, 102px 68px 0 0 #FF9E9D, 102px 85px 0 0 #DAD8A7, 102px 102px 0 0 #7FC7AF, 102px 119px 0 0 #3FB8AF, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #DAD8A7, 119px 34px 0 0 #7FC7AF, 119px 51px 0 0 #3FB8AF, 119px 68px 0 0 #FF3D7F, 119px 85px 0 0 #FF9E9D, 119px 102px 0 0 #DAD8A7, 119px 119px 0 0 #7FC7AF;}
60% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #DAD8A7, 17px 34px 0 0 #7FC7AF, 17px 51px 0 0 #3FB8AF, 17px 68px 0 0 #FF3D7F, 17px 85px 0 0 #FF9E9D, 17px 102px 0 0 #DAD8A7, 17px 119px 0 0 #7FC7AF, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #FF9E9D, 34px 34px 0 0 #DAD8A7, 34px 51px 0 0 #7FC7AF, 34px 68px 0 0 #3FB8AF, 34px 85px 0 0 #FF3D7F, 34px 102px 0 0 #FF9E9D, 34px 119px 0 0 #DAD8A7, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #FF3D7F, 51px 34px 0 0 #FF9E9D, 51px 51px 0 0 #DAD8A7, 51px 68px 0 0 #7FC7AF, 51px 85px 0 0 #3FB8AF, 51px 102px 0 0 #FF3D7F, 51px 119px 0 0 #FF9E9D, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #3FB8AF, 68px 34px 0 0 #FF3D7F, 68px 51px 0 0 #FF9E9D, 68px 68px 0 0 #DAD8A7, 68px 85px 0 0 #7FC7AF, 68px 102px 0 0 #3FB8AF, 68px 119px 0 0 #FF3D7F, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #7FC7AF, 85px 34px 0 0 #3FB8AF, 85px 51px 0 0 #FF3D7F, 85px 68px 0 0 #FF9E9D, 85px 85px 0 0 #DAD8A7, 85px 102px 0 0 #7FC7AF, 85px 119px 0 0 #3FB8AF, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #DAD8A7, 102px 34px 0 0 #7FC7AF, 102px 51px 0 0 #3FB8AF, 102px 68px 0 0 #FF3D7F, 102px 85px 0 0 #FF9E9D, 102px 102px 0 0 #DAD8A7, 102px 119px 0 0 #7FC7AF, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #FF9E9D, 119px 34px 0 0 #DAD8A7, 119px 51px 0 0 #7FC7AF, 119px 68px 0 0 #3FB8AF, 119px 85px 0 0 #FF3D7F, 119px 102px 0 0 #FF9E9D, 119px 119px 0 0 #DAD8A7;}
80% {box-shadow: 0px 0px 0 0 rgba(255,255,255,0), 0px 17px 0 0 rgba(255,255,255,0), 0px 34px 0 0 rgba(255,255,255,0), 0px 51px 0 0 rgba(255,255,255,0), 0px 68px 0 0 rgba(255,255,255,0), 0px 85px 0 0 rgba(255,255,255,0), 0px 102px 0 0 rgba(255,255,255,0), 0px 119px 0 0 rgba(255,255,255,0), 17px 0px 0 0 rgba(255,255,255,0), 17px 17px 0 0 #FF9E9D, 17px 34px 0 0 #DAD8A7, 17px 51px 0 0 #7FC7AF, 17px 68px 0 0 #3FB8AF, 17px 85px 0 0 #FF3D7F, 17px 102px 0 0 #FF9E9D, 17px 119px 0 0 #DAD8A7, 34px 0px 0 0 rgba(255,255,255,0), 34px 17px 0 0 #FF3D7F, 34px 34px 0 0 #FF9E9D, 34px 51px 0 0 #DAD8A7, 34px 68px 0 0 #7FC7AF, 34px 85px 0 0 #3FB8AF, 34px 102px 0 0 #FF3D7F, 34px 119px 0 0 #FF9E9D, 51px 0px 0 0 rgba(255,255,255,0), 51px 17px 0 0 #3FB8AF, 51px 34px 0 0 #FF3D7F, 51px 51px 0 0 #FF9E9D, 51px 68px 0 0 #DAD8A7, 51px 85px 0 0 #7FC7AF, 51px 102px 0 0 #3FB8AF, 51px 119px 0 0 #FF3D7F, 68px 0px 0 0 rgba(255,255,255,0), 68px 17px 0 0 #7FC7AF, 68px 34px 0 0 #3FB8AF, 68px 51px 0 0 #FF3D7F, 68px 68px 0 0 #FF9E9D, 68px 85px 0 0 #DAD8A7, 68px 102px 0 0 #7FC7AF, 68px 119px 0 0 #3FB8AF, 85px 0px 0 0 rgba(255,255,255,0), 85px 17px 0 0 #DAD8A7, 85px 34px 0 0 #7FC7AF, 85px 51px 0 0 #3FB8AF, 85px 68px 0 0 #FF3D7F, 85px 85px 0 0 #FF9E9D, 85px 102px 0 0 #DAD8A7, 85px 119px 0 0 #7FC7AF, 102px 0px 0 0 rgba(255,255,255,0), 102px 17px 0 0 #FF9E9D, 102px 34px 0 0 #DAD8A7, 102px 51px 0 0 #7FC7AF, 102px 68px 0 0 #3FB8AF, 102px 85px 0 0 #FF3D7F, 102px 102px 0 0 #FF9E9D, 102px 119px 0 0 #DAD8A7, 119px 0px 0 0 rgba(255,255,255,0), 119px 17px 0 0 #FF3D7F, 119px 34px 0 0 #FF9E9D, 119px 51px 0 0 #DAD8A7, 119px 68px 0 0 #7FC7AF, 119px 85px 0 0 #3FB8AF, 119px 102px 0 0 #FF3D7F, 119px 119px 0 0 #FF9E9D;}

}


```

``` html

<!-- Created in shadowPainter : ) -->
<div class='box'><span class='dot'></span></div>


```

## circle loading

``` css
$cirle-width: 95vmin;

// You can play with these for a little variation
$shadow-depth: $cirle-width * .125;
$shadow-depth-hover-ratio: 2;
$shadow-blur: $shadow-depth * 0;
$shadow-spread: $shadow-depth * 0;

$y-offset: $shadow-depth * .5;
$x-offset: $y-offset * 1.7320508076; // √3
$y-offset-hover: $y-offset * $shadow-depth-hover-ratio;
$x-offset-hover: $x-offset * $shadow-depth-hover-ratio;

$red:    rgba(255,   0,   0, .45);
$orange: rgba(253, 127,  11, .54);
$yellow: rgba(235, 255,   0, .54);
$green:  rgba( 22, 243,   3, .55);
$blue:   rgba(  0, 133, 255, .53);
$purple: rgba(190,  11, 224, .55);

* {
  box-sizing: border-box;
}

html, body {
  height: 100%;
  margin: 0;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  background: radial-gradient(ellipse at center, #fff 0%,#eee 80%);
}

@keyframes spin {
    0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

.circle {
  position: relative;
  width: $cirle-width;
  border-radius: 50%;
  transition: all .3s ease;
  box-shadow:
    inset $x-offset (-$y-offset) $shadow-blur $shadow-spread $red,
    inset (-$x-offset) (-$y-offset) $shadow-blur $shadow-spread $yellow,
    inset 0 $shadow-depth $shadow-blur $shadow-spread $blue,
    inset (-$x-offset) $y-offset $shadow-blur $shadow-spread $green,
    inset $x-offset $y-offset $shadow-blur $shadow-spread $purple,
    inset 0 (-$shadow-depth) $shadow-blur $shadow-spread $orange,
  ;
  animation: spin 120s linear infinite;
  
  &:hover {
    box-shadow:
      inset $x-offset-hover (-$y-offset-hover) $shadow-blur $shadow-spread $red,
      inset (-$x-offset-hover) (-$y-offset-hover) $shadow-blur $shadow-spread $yellow,
      inset 0 ($shadow-depth * $shadow-depth-hover-ratio) $shadow-blur $shadow-spread $blue,
      inset (-$x-offset-hover) $y-offset-hover $shadow-blur $shadow-spread $green,
      inset $x-offset-hover $y-offset-hover $shadow-blur $shadow-spread $purple,
      inset 0 (-$shadow-depth * $shadow-depth-hover-ratio) $shadow-blur $shadow-spread $orange,
    ;
  }
  
  &:before {
    content: "";
    display: block;
    padding-top: 100%;
  }
}

```
``` html
<div class="circle"></div>

```
