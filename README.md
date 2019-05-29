# quartz-cluster
扩展quartz动态分布式定时任务
常规使用quartz需要每一个任务都实现org.quartz.Job接口，每次添加，删除或者修改任务配置都需要停机修改代码再重新部署，即使quartz提供API可以运行时删除或修改，但是机器重启后，只要代码不修改，还是会恢复成初始的配置。
所以针对以上的问题，最好是能做成动态可配置的才能更方便地管理我们的定时任务。**最好的结果是可以直接使用spring管理的任意Bean对象，通过Bean的名称，指定的方法名，就能按照一定的调度策略执行定时任务**。

使用方式：

**1.先导入依赖：**
```
<dependency>
    <groupId>com.github.zw201913</groupId>
    <artifactId>quartz-cluster</artifactId>
    <version>1.0.1.RELEASE</version>
</dependency>
```








