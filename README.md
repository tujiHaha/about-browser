# about-browser
关于浏览器工作的知识

## 回收堆内存中的数据 就要用到垃圾回收器

### 代际假说  分代收集

<!-- 代际假说 -->
1. 大部分对象在内存中的时间很短 很快就变得不可访问
2. 不死的对象 回活得更久

**算法很多各有千秋 v8把堆分成新生代 老生代 新生代时间短对象 老生代时间久对象**

**新生代小-- 副垃圾回收器 老生代大--主垃圾回收器**

***1标记活动对象 非活动对象***
***2清理非活动内存 3整理内存碎片***

## 副垃圾回收器 新生代 scavenge算法
### 新生区 对象区 空闲区 新加入的对象放对象区 快写满的时候 把活动对象复制到空闲区 新生区对象占内存小 

### 老生区 mark-sweep 标记-清除法 标记-整理

## 全停顿

## 增量标记算法
