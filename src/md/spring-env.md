### 核心组件

* PropertySource 和 PropertyResolver
    * PropertySource：对 key-value 资源的封装，一个项目中往往有多种不同的资源格式
        * 存储的是未处理过的数据
    * PropertySources：组合模式，统一管理 PropertySource 增删改
    * PropertyResolver：中间层，间接地从 PropertySource 获取 value。暴露给客户端使用
        * 充当门面，为 PropertySources 提供查的能力
        * 在获取数据的时候，可以做一些处理，比如说占位符
    * Profiles 提供环境隔离的能力
        
* Environment 通过组合 PropertySources、PropertyResolver、Profiles 方便开发人员使用

* Resource 和 ResourceLoader
    * Resource 是对资源的封装，这里的资源格式是不确定的
    * ResourceLoader 主要是从各种渠道获取到各种格式的 Resource
    
* PropertySourceLoader 通过解析 Resource 获得 PropertySource