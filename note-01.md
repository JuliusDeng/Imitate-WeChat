# weex/nvue  笔记

# 1 view里面的style不支持``模板字符串写法  
# eg：view :style=`'height':${statusBarHeight}'px'`></view> // 不生效，未知bug
# computed中当然可以写``模板字符串写法

# 2 [官方已说不要太依赖rpx 如高度和字体是不应该根据屏幕宽度（等比）变化的](https://ask.dcloud.net.cn/article/36130)顺便提醒另一个事情，很多开发者对响应式单位依赖太严重了，比如组件高度或字体大小也使用upx/rpx。 注意只有当你需要某元素的单位要根据屏幕宽度（小范围）大小变化时，才需要rpx这类动态宽度单位。 一般情况下高度和字体大小是不应该根据屏幕宽度（等比）变化的。

# 3 注：<slot></slot>组件默认在外层家里<text></text>,实际是如此：<text><slot></slot></text>  而<text>组件不可内嵌自身。
