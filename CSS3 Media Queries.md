常用主流移动设备CSS3 Media Queries整理

使用的时候根据实际的需要进行条件判断，其中 
landscape 表示设备 横屏 情况 ，portrait 表示设备 竖屏 情况

max-device-width 表示设备最大分辨率宽度，min-device-width 表示设备最小分辨率宽度

关于 min-width 和 min-device-width 的区别是，前者是指的网页窗口的最小宽度，后者是指设备最小分辨率宽度，同理 max-width 和 max-device-width，前者是指网页窗口的最大宽度，后者是指设备最大分辨率宽度。

值得注意的是 我们在写设备页面适配的时候，不要忘记加上这句，要不然页面在PC端模拟测试是没有效果的。

``html
<meta name="viewport" content="width=device-width,user-scalable=no" />
``
意思是：设置屏幕宽度为设备宽度，禁止用户手动调整缩放，关于viewpotr其他具体参数设置，可以百度查阅。

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
