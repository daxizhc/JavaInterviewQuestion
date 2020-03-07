## 面试题

新生代分为几个区？使用什么算法进行垃圾回收？为什么使用这个算法？

## 解析

新生代分为survivor区和eden区，survivor区又分为相等的from和to两块区域。  
新生代使用复制算法来进行垃圾回收，复制算法的优点是不用考虑碎片问题，方法简单高效，缺点是内存浪费严重。  
因为一般有98%的新生代对象是可回收的，Hotspot默认survivor区和eden区大小比例是2:8，这样既避免了内存浪费，又避免了碎片问题。