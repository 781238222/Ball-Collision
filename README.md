# Ball-Collision
小球碰撞，类似于windows平台的屏保效果

![效果：](https://github.com/781238222/Ball-Collision/blob/master/gif/1.gif)


如果你想要改变效果，只需要重写createBalls方法。目前支持bitmap和shape，优先bitmap。

注意：

1、小球在初始化时不能让小球重叠，小球默认位置是随机的，所以要控制好view的大小、小球半径及个数。createBalls方法
    是可能有死循环的。
    
2、小球的速度并不是每秒走的距离，而是每帧，也就意味着不同的设备看起来的速度是不一样的，高帧率的设备要快一些，
    解决办法（代码中未实现，提供一种解决思路，如果有好的思路欢迎分享）：
    开启独立线程更新速度及位置，但要注意onDraw方法不要在正在更新速度、位置是进行