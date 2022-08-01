### 前提
- 小车的坐标点
- Path的理解
- 对一些任务比较熟悉

### Path中涉及的常用算法
- 对Path进行运行，如平移Path，剪切path，添加路径段
- 场景：自适应取放货，扫码，超高超宽等检测任务，提前放置货物，货柜车装车（库位存在偏移的情况）
- 涉及的配置或者任务特性
    - CutDistance, CutDistanceOfXXX
        - 截取最后一段直线路径（倒车，最大截取的距离为最后一段路径的长度）
    - LiftStartDistance, LiftStartDistanceOfXXX
        - 距离车开始移动的距离
    - 获取感知位（检测位）
    - 开始扫码距离
    - 