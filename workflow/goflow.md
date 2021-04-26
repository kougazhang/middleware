# goflow

## 组件

+ DB, 保存图执行的节点
+ broker 通信

## Runtime

+ Register: 把 workload (工作函数) 注册到 node.

  + workload 对参数类型进行了限制. 代码示例:

    ```
    f.SyncNode().Apply("test", doSomething)
    ```

  + workload 注册到了 `FlowService.Flows` 上.

  + 注册这个步骤在 gleam 也有, 对应的是 map, reduce 等算子对应的具体函数.

+ 解析 dag

## 构思

看懂 goflow 到底是怎么解析 dag 执行的. 把这部分代码和 machinery 结合起来不就是 golang 版的 airflow 了吗.

解析 goflow 后, 把所有的变成 callback url. 执行完本函数后进行回调.

## 第三方

+ Gographziv, 把 graphziv 转为 go ast. 
+ [分布式任务调度系统之任务编排及工作流实现原理与 golang 实践](https://github.com/skyhackvip/dag) 配有文字说明, 易懂, 介绍了图的基础知识
+ [LiteFlow](https://github.com/yueyunyue/liteflow) 是一个基于任务版本来实现的分布式任务流调度系统, java 实现, 前端可拖拽, java + react
+ [dag](https://github.com/goombaio/dag) golang 实现 start 最高, 但是无遍历
+ [clock](https://github.com/BruceDone/clock) golang + vue, 功能同 LiteFlow.
+ [glow](https://github.com/chrislusf/glow) 还能生成 dag 图
+ [dag](https://github.com/mostafa-asg/dag) 简化了 dag 的组织成本, 封装了不错的 API.

