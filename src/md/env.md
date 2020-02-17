### 核心组件

* PropertySource 和 PropertyResolver
    * PropertySource：对 key-value 资源的封装，一个项目中往往有多种不同的资源格式
    * PropertyResolver：中间层，间接地从 PropertySource 获取 value。暴露给客户端使用

* Resource 和 ResourceLoader
    * Resource 是对资源的封装，这里的资源格式是不确定的
    * ResourceLoader 主要是从各种渠道获取到各种格式的 Resource