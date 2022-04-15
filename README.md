# GoFound

`GoFound` 一个golang实现的全文检索引擎，支持持久化和单机亿级数据毫秒级查找。
接口可以通过http调用。详见 [API文档](./docs/api.md)

## 文档

+ [示例](./docs/example.md)
+ [API文档](./docs/api.md)
+ [索引原理](./docs/index.md)
+ [配置文档](./docs/config.md)
+ [持久化](./docs/storage.md)
+ [编译部署](./docs/compile.md)

## 技术栈

+ 平衡二叉查找树
+ 二分法查找
+ 快速排序法
+ 倒排索引
+ 正排索引
+ 文件分片
+ golang-jieba分词
+ leveldb

### 为何要用golang实现一个全文检索引擎？

+ 正如其名，`GoFound`去探索全文检索的世界，一个小巧精悍的全文检索引擎，支持持久化和单机亿级数据毫秒级查找。

+ 传统的项目大多数会采用`ElasticSearch`来做全文检索，因为`ElasticSearch`够成熟，社区活跃、资料完善。缺点就是配置繁琐、基于JVM对内存消耗比较大。

+ 所以我们需要一个更高效的搜索引擎，而又不会消耗太多的内存。 以最低的内存达到全文检索的目的，相比`ElasticSearch`，`gofound`是原生编译，会减少系统资源的消耗。而且对外无任何依赖。

## 安装和启动

> 下载好源码之后，进入到源码目录，执行下列两个命令
>

+ 编译

```shell
go build
```

+ 启动

```shell
./go_search --addr=:8080 --path=./data
```

+ 其他命令
  参考 [配置文档](./docs/config.md)

## 客户端
[GoFound Python客户端](https://github.com/newpanjing/gofound-python)

## 使用GoFound的用户

[Simple社区](https://simpleui.72wo.com)
[贝塔博客](https://www.88cto.com)
[Book360](https://www.book360.cn)
[十二点科技](https://www.72wo.com)
[恒一博科技](http://www.hooebo.com)