# 为解决retina屏边框1px显示较粗问题，经过各种选择和尝试应用，终于找到一个非常好的解决方案
效果见[index.html](https://github.com/maweimaweima/1px-border/blob/master/index.html)

    使用伪类生成的边框，可以实现边框的上下左右和圆角。再通过sass的mixin辅助，使用起来非常方便。
    最后是在兼容方面也都顺利解决。
    1.对有边框的需增加border-handle类，对input等无子元素的边框需增加类名称为border-handle的父元素
    2.需保证border-handle有明确的宽和高，否则会导致边框不正常
    3.对一些子元素被边框覆盖，设置下子元素的层级则可
    4.对比例精度需设置较高，如33.333333%
    5.sass 混合borderHandle使用
    	$borderWidthes 设置4个边
    	$borderColor 设置边颜色
    	$radius 设置圆角
    6.对list应该优先使用top和left做边，否则容易导致ios中边不对齐
