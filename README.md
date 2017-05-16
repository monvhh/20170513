# 20170513
H5项目

20170513开始做的一个H5项目，耗时>16h，因为中间有需求变更，再加上兼容问题。

遇到的两个兼容问题及解决办法：

* zepto中swipe在苹果手机上无效
加入以下代码

```
document.addEventListener('touchmove', function (event) {
event.preventDefault();
}, false);
```

* 苹果手机微信不播放音乐
加入以下代码

```
document.getElementById('car_audio').play();
wx.ready(function(){
    document.getElementById('car_audio').play();
})
```
