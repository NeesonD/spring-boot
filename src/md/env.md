### 核心组件

* PropertySource 和 PropertyResolver
    * PropertySource：对 key-value 资源的封装，一个项目中往往有多种不同的资源格式
        * 存储的是原滋原味的数据
    * PropertyResolver：中间层，间接地从 PropertySource 获取 value。暴露给客户端使用
        * 充当门面
        * 在获取数据的时候，可以做一些处理，比如说占位符
        
* PropertyResolver 是一个小门面，Environment 是一个集大成者的大门面

* Resource 和 ResourceLoader
    * Resource 是对资源的封装，这里的资源格式是不确定的
    * ResourceLoader 主要是从各种渠道获取到各种格式的 Resource