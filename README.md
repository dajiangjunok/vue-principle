# vue-principle

观察者模式和发布订阅的区别：
观察者模式中，发布者和订阅着是相互依赖的，必须要求观察者订阅内容改变事件，
并且发布 订阅者是由调度中心进行调度，也就是说调度中心调用观察者列表中的每个观察着，触发其更新事件
大白话：一个对象（观察者）订阅另一个对象（主题），当主题被激活的时候，触发观察者里面的事件。

发布订阅模式则不同，是由发布者，信息中心，订阅者构成，通过$on 监听事件将发布者和回调函数放入了信息中心(相当于关注),
然后发布者通过$emit 发射事件，此时信息中心的订阅者集合就会根据发布者信息调用对应所有订阅者的回调函数，从而达到通知订阅者的工作
大白话：订阅者把自己想要订阅的事件注册到调度中心，当发布者发布事件到调度中心（就是该事件被触发），再由调度中心统一调度订阅者注册到调度中心的处理代码。
