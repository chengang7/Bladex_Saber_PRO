<template>
  <div>
    <el-row>
      <el-col :span="24">
        <third-register></third-register>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <basic-container>
          <p style="text-align: center">
            <img src="https://img.shields.io/badge/Release-V2.8.1-green.svg" alt="Downloads"/>
            <img src="https://img.shields.io/badge/JDK-1.8+-green.svg" alt="Build Status"/>
            <img src="https://img.shields.io/badge/Spring%20Cloud-Hoxton.SR11-blue.svg" alt="Coverage Status"/>
            <img src="https://img.shields.io/badge/Spring%20Boot-2.2.13.RELEASE-blue.svg" alt="Downloads"/>
            <a target="_blank" href="https://bladex.vip">
              <img src="https://img.shields.io/badge/Saber%20Author-Small%20Chill-ff69b4.svg" alt="Downloads"/>
            </a>
            <a target="_blank" href="https://bladex.vip">
              <img src="https://img.shields.io/badge/Copyright%20-@BladeX-%23ff3f59.svg" alt="Downloads"/>
            </a>
          </p>
        </basic-container>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="16">
        <basic-container>
          <el-collapse v-model="activeNames" @change="handleChange">
            <el-collapse-item title="欢迎使用Saber" name="1">
              <div>1.Saber是BladeX前端UI系统</div>
              <div>2.对现有的avue2.0、element-ui库进行二次封装</div>
              <div>3.100%兼容原生element-ui库</div>
              <div>4.基于json驱动的模块配置，打造最好用的vuejs中后台脚手架</div>
              <div>5.使用Saber可以大幅度提升开发效率，不再为重复工作发愁</div>
            </el-collapse-item>
            <el-collapse-item title="什么是BladeX" name="2">
              <div>1.BladeX是一款精心设计的微服务架构，提供 SpringCloud 全套解决方案</div>
              <div>2.开源中国首批完美集成 SpringCloud Alibaba 系列组件的微服务架构</div>
              <div>3.基于稳定生产的商业项目升级优化而来，更加贴近企业级的需求</div>
              <div>4.追求企业开发更加高效，部署更加方便，生产更加稳定</div>
              <div>5.GVP-码云最有价值开源项目</div>
              <div>6.BladeX授权地址:<a target="_blank" href="https://bladex.vip/#/vip">点击授权</a></div>
            </el-collapse-item>
            <el-collapse-item title="为何需要BladeX" name="3">
              <div>1.经历过较长的线上生产，积累了很多企业痛点的解决方案</div>
              <div>2.一套代码兼容MySql、Oracle、PostgreSQL、SqlServer，适应企业各种不同场景的需求</div>
              <div>3.集成了很多企业急切所需的例如多租户、Oauth2授权认证、工作流、分布式事务等等功能</div>
              <div>4.深度定制了Flowable工作流，完美支持SpringCloud分布式服务的场景，以远程调用的方式进行操作</div>
              <div>5.升级了核心驱动，新功能完全可以开箱即用，而开源版需要自己再花时间进行集成，需要花掉更多的时间成本</div>
              <div>6.拥抱微服务时代，很多企业由于项目转型或升级，传统的技术已然不能满足，反而会花更多成本，而BladeX就是为此而生</div>
              <div>7.同时提供SpringCloud版本和SpringBoot版本，两个版本的api可以与Sword和Saber无缝对接，为小型项目至大型项目保驾护航</div>
              <div>8.授权购买即永久，源码没有混淆，完全开放，后续升级完全免费。企业只需花很少的钱即可获得一整套成熟的解决方案，你还在等什么？</div>
            </el-collapse-item>
            <el-collapse-item title="拥有的核心功能" name="4">
              <div>1.前后端分离-采用前后端分离模式，前端提供两套架构，Sword基于React，Saber基于Vue</div>
              <div>2. 分布式单体式后端架构-提供两套后端架构，基于SpringCloud的分布式架构以及基于SpringBoot的单体式架构</div>
              <div>3.API完全兼容-两套后端架构与两套前端架构，共四套架构可以任意组合，所有API完全兼容</div>
              <div>4.前后端代码生成-定制针对两套前端与后端的代码生成模板，轻松生成整个模块的前后端代码，减少重复工作量</div>
              <div>5.组件化、插件化架构-针对功能深度定制各个starter，引入开箱即用，为整个架构解耦，提升效率</div>
              <div>6.Nacos-集成阿里巴巴的Nacos完成统一的服务注册与配置</div>
              <div>7.Sentinel-集成Sentinel从流量控制、熔断降级、系统负载等多个维度保护服务的稳定性</div>
              <div>8.Dubbo-完美集成Dubbo最新版，支持远程RPC调用</div>
              <div>9.多租户系统-完整的SaaS多租户架构</div>
              <div>10.Oauth2-集成Oauth2协议，完美支持多终端的接入与认证授权</div>
              <div>11.工作流-深度定制SpringCloud分布式场景的Flowable工作流，为复杂流程保驾护航。同时提供SpringBoot集成版本</div>
              <div>12.独立流程设计器-提供独立的完全汉化的流程设计器，轻松定制流程模型</div>
              <div>13.动态网关-集成基于Nacos的轻量级、高拓展性动态网关</div>
              <div>14.动态聚合文档-实现基于Nacos的Swagger SpringCloud聚合文档</div>
              <div>15.分布式文件服务-集成minio、qiniu、alioss等优秀的第三方，提供便捷的文件上传与管理</div>
              <div>16.多租户对象存储系统-在SaaS系统中，各租户可自行配置文件上传至自己的私有OSS</div>
              <div>17.权限管理-精心设计的权限管理方案，角色权限精确到按钮</div>
              <div>18.动态数据权限-高度灵活的动态数据权限，提供注解+Web可视化两种配置方式，Web配置无需重启直接生效</div>
              <div>19.动态接口权限-高度灵活的动态接口权限，提供注解+Web可视化两种配置方式，Web配置无需重启直接生效</div>
              <div>20.多租户顶部菜单配置-提供给每个租户独立的顶部菜单配置模块，可以自定义顶部菜单切换</div>
              <div>21.主流数据库兼容-一套代码完全兼容Mysql、Postgresql、Oracle三大主流数据库</div>
              <div>22.动态网关鉴权-基于Nacos的动态网关鉴权，可在线配置，实时生效</div>
              <div>23.全能代码生成器-支持自定义模型、模版 、业务建模，支持多种模板引擎，在线配置。大幅度提升开发效率，不再为重复工作发愁</div>
              <div>24.Seata分布式事务-定制集成Seata，支持分布式事务，无代码侵入，不失灵活与简洁</div>
              <div>25.未完待续...</div>
            </el-collapse-item>
            <el-collapse-item title="软件定制开发合作" name="5">
              <div>1.接BladeX系列架构的定制服务</div>
              <div>2.接3个月以内工期的react、vue、springboot、springcloud、app、小程序等软件定制服务</div>
              <div>3.有意向请联系唯一指定QQ:1272154962</div>
            </el-collapse-item>
          </el-collapse>
        </basic-container>
      </el-col>
      <el-col :span="8">
        <el-row>
          <basic-container>
            <div class="el-font-size">
              <span>产品名称</span>
              <el-divider direction="vertical"/>
              <span><el-tag>BladeX企业级微服务开发平台</el-tag></span>
              <el-divider content-position="right"><i class="el-icon-star-off"/></el-divider>
              <span>账号密码</span>
              <el-divider direction="vertical"/>
              <el-tag type="info" effect="plain">人事(hr)</el-tag>
              <el-divider direction="vertical"/>
              <el-tag type="success" effect="plain">经理(manager)</el-tag>
              <el-divider direction="vertical"/>
              <el-tag type="warning" effect="plain">老板(boss)</el-tag>
              <el-divider content-position="right"><i class="el-icon-star-off"/></el-divider>
              <span>官网地址</span>
              <el-divider direction="vertical"/>
              <span><el-link href="https://bladex.vip" target="_blank"
                             type="primary">https://bladex.vip</el-link></span>
              <el-divider content-position="right"><i class="el-icon-star-off"/></el-divider>
              <span>社区地址</span>
              <el-divider direction="vertical"/>
              <span><el-link href="https://sns.bladex.vip" target="_blank"
                             type="primary">https://sns.bladex.vip</el-link></span>
              <el-divider content-position="right"><i class="el-icon-star-off"/></el-divider>
              <span>获取文档</span>
              <el-divider direction="vertical"/>
              <span class="tag-group">
                <el-tag type="success" style="cursor: pointer"
                        onclick="window.open('https://sns.bladex.vip/note/view/1.html')">免费版</el-tag>
                <el-divider direction="vertical"/>
                <el-tag type="danger" style="cursor: pointer"
                        onclick="window.open('https://www.kancloud.cn/@smallchill')">收费版</el-tag>
              </span>
              <el-divider content-position="right"><i class="el-icon-star-off"/></el-divider>
              <span>获取源码</span>
              <el-divider direction="vertical"/>
              <span class="tag-group">
                <el-tag type="success" effect="dark" style="cursor: pointer"
                        onclick="window.open('https://gitee.com/smallc/SpringBlade')">开源版</el-tag>
                <el-divider direction="vertical"/>
                <el-tag type="danger" effect="dark" style="cursor: pointer"
                        onclick="window.open('https://bladex.vip/#/vip')">商业版</el-tag>
              </span>
            </div>
          </basic-container>
        </el-row>
        <el-row>
          <basic-container>
            <el-collapse v-model="logActiveNames" @change="handleChange">
              <el-collapse-item title="2.8.1.RELEASE发布，适配Nacos2支持长链接特性" name="23">
                <div>1.[升级]SpringCloud 至 Hoxton.SR11</div>
                <div>2.[升级]Avue 至 2.8.12</div>
                <div>3.[升级]Lombok 至 1.18.18</div>
                <div>4.[升级]Nacos 至 2.0.1</div>
                <div>5.[升级]JustAuth 至 1.16.1</div>
                <div>6.[新增]JustAuth支持基于redis的state缓存</div>
                <div>7.[新增]服务内部调用文件上传的工具类</div>
                <div>8.[新增]插件市场目录说明</div>
                <div>9.[新增]全新布局的字典管理模块</div>
                <div>10.[优化]Dockerfile初始镜像改为固化的openjdk8-openj9含字体版本</div>
                <div>11.[优化]SmsResponse返回字段message为msg</div>
                <div>12.[优化]Feign熔断加载逻辑</div>
                <div>13.[优化]Sql打印插件增加java8时间处理</div>
                <div>14.[优化]多数据源环境下生效Sql打印插件的配置</div>
                <div>15.[优化]校验短信验证码时与手机号关联验证</div>
                <div>16.[优化]Request包装逻辑支持配置跳过</div>
                <div>17.[优化]Mybatis-plus的SQLServerDialect逻辑</div>
                <div>18.[优化]ObjectMapper支持可配</div>
                <div>19.[优化]增加跨域请求头以防独立swagger服务出现跨域</div>
                <div>20.[优化]数据权限与接口权限的缓存改为全局</div>
                <div>21.[优化]Xss过滤逻辑</div>
                <div>22.[优化]角色配置逻辑</div>
                <div>23.[优化]菜单配置逻辑</div>
                <div>24.[修复]ImageUtil宽高反转的bug</div>
                <div>25.[修复]树组件未全选导致父节点没有入库从而引发顶部菜单生成的bug</div>
                <div>26.[修复]字典通用接口未返回id与parentId产生的bug</div>
                <div>27.[脚本]启动脚本增加jvm配置</div>
                <div>28.[脚本]修复report脚本部署逻辑</div>
                <div>29.[移除]过时的BladeRedisCache，请用BladeRedis取代</div>
              </el-collapse-item>
              <el-collapse-item title="2.8.0.RELEASE发布，集成Prometheus全方位监控方案" name="22">
                <div>1.[升级]SpringCloud 至 Hoxton.SR10</div>
                <div>2.[升级]AlibabaCloud 至 2.2.5.RELEASE</div>
                <div>3.[升级]FastJson 至 1.2.75</div>
                <div>4.[升级]Druid 至 1.2.5</div>
                <div>5.[升级]EasyExcel 至 1.2.7</div>
                <div>6.[升级]JustAuth 至 1.15.9</div>
                <div>7.[升级]Avue 至 2.8.1</div>
                <div>8.[升级]ElementUI 至 2.15.1</div>
                <div>9.[升级]Oss与Sms升级依赖并适配最新版</div>
                <div>10.[新增]基于宝塔系统的部署方案</div>
                <div>11.[新增]Prometheus全方位监控方案</div>
                <div>12.[新增]blade-admin服务支持prometheus对nacos的服务发现</div>
                <div>13.[新增]BladeX对接Prometheus部署脚本</div>
                <div>14.[新增]Saber远程部署推送脚本</div>
                <div>15.[新增]基于Sentinel的服务熔断方案</div>
                <div>16.[新增]Mybatis-Plus添加OptimizeJoin配置参数</div>
                <div>17.[优化]将oss-starter系列合并为一</div>
                <div>18.[优化]将sms-starter系列合并为一</div>
                <div>19.[优化]增强优化Url通配符匹配逻辑</div>
                <div>20.[优化]数据权限缓存逻辑</div>
                <div>21.[优化]blade-auto封装</div>
                <div>22.[优化]SqlLogInterceptor配置</div>
              </el-collapse-item>
              <el-collapse-item title="2.7.2.RELEASE发布，重构升级常用功能，优化使用体验" name="21">
                <div>1.[升级]SpringBoot 至 2.2.13.RELEASE</div>
                <div>2.[升级]AlibabaCloud 至 2.2.5</div>
                <div>3.[升级]Mybatis-Plus 至 3.4.2</div>
                <div>4.[升级]Dynamic-Datasource 至3.3.1</div>
                <div>5.[升级]Avue 至 2.7.8</div>
                <div>6.[升级]适配 Knife4j 2.0.8</div>
                <div>7.[重构]Swagger聚合网关迁移至全新的blade-swagger服务</div>
                <div>8.[重构]Sql日志打印采用druid底层实现展示完整带参SQL</div>
                <div>9.[新增]LocalFile的domain字段</div>
                <div>10.[新增]Sign模式鉴权timestamp在10秒内的合法时间段判断</div>
                <div>11.[新增]开启租户插件后使用@TenantIgnore注解精准关闭租户过滤逻辑</div>
                <div>12.[新增]Swagger公共信息配置</div>
                <div>13.[新增]Saber矢量图标离线化</div>
                <div>14.[新增]菜单管理isOpen字段控制左侧菜单是否可以使用新tab打开外链</div>
                <div>15.[新增]Mybatis-Plus的Page合并工具类</div>
                <div>16.[优化]阿里云短信返回成功判断逻辑</div>
                <div>17.[优化]Token过期时间处理</div>
                <div>18.[优化]Redis加载逻辑</div>
                <div>19.[优化]用户登录逻辑</div>
                <div>20.[优化]多租户角色创建逻辑</div>
                <div>21.[优化]Dockerfile加速字体构建</div>
                <div>22.[优化]Nacos Shared Config配置API改为最新版</div>
                <div>23.[优化]Saber授权类型字段改为checkbox</div>
                <div>24.[修复]RequestLog遇到MultipartFile.[]类型序列化报错的问题</div>
                <div>25.[修复]顶级字典更新后未同步更新下属字典的编号</div>
                <div>26.[修复]Saber退出后未刷新浏览器顶部title路由的问题</div>
                <div>27.[修复]菜单机构模块关闭编辑界面再打开新增界面数据没有清空的问题</div>
              </el-collapse-item>
              <el-collapse-item title="2.7.1.RELEASE发布，重构钉钉监控通知，升级依赖适配最新API" name="20">
                <div>1.[升级]SpringBoot 至 2.2.12.RELEASE</div>
                <div>2.[升级]SpringCloud 至 Hoxton.SR9</div>
                <div>3.[升级]Knife4j 至 2.0.8</div>
                <div>4.[升级]Druid 至 1.2.4</div>
                <div>5.[升级]Seata 至 1.4.1</div>
                <div>6.[升级]Jackson 至 2.11.4</div>
                <div>7.[升级]Mybatis-Plus 至 3.4.1</div>
                <div>8.[升级]Dynamic-Datasource 至3.2.1</div>
                <div>9.[升级]Avue 至 2.7.5</div>
                <div>10.[新增]Secure模块动态签名认证特性</div>
                <div>11.[新增]Redis序列化方式的配置</div>
                <div>12.[新增]用户导入导出的用户平台字段</div>
                <div>13.[修改]日志路径默认优先级，支持配置覆盖</div>
                <div>14.[修改]Report模块包路径，新增Core目录</div>
                <div>15.[重构]blade-admin，钉钉监控通知实现</div>
                <div>16.[优化]blade-admin，增加账号密码登录</div>
                <div>17.[优化]RefreshToken刷新逻辑</div>
                <div>18.[优化]租户新增逻辑，业务字典支持无限层级复制</div>
                <div>19.[优化]Ribbon组件，支持Feign调用配置</div>
                <div>20.[修复]流程名搜索失效的问题</div>
                <div>21.[修复]附件管理租户隔离问题</div>
                <div>22.[修复]数据权限分配模块的sqlserver兼容性</div>
                <div>23.[修复]系统字典缓存刷新逻辑</div>
                <div>24.[修复]Swagger文档出现Locale参数的问题</div>
                <div>25.[删除]spring-cloud-stream依赖，按需引入</div>
              </el-collapse-item>
              <el-collapse-item title="2.7.0.RELEASE发布，更新Hoxton.SR8，全面升级底层驱动" name="19">
                <div>1.[升级]SpringBoot 至 2.2.11.RELEASE</div>
                <div>2.[升级]SpringCloud 至 Hoxton.SR8</div>
                <div>3.[升级]AlibabaCloud 至 2.2.3.RELEASE</div>
                <div>4.[升级]SpringBootAdmin 至 2.2.4</div>
                <div>5.[升级]Knife4j 至 2.0.6</div>
                <div>6.[升级]Swagger 至 2.10.5</div>
                <div>7.[升级]SwaggerModel 至 1.6.2</div>
                <div>8.[升级]SpringPlugin 至 2.2.0.RELEASE</div>
                <div>9.[升级]Druid 至 1.2.1</div>
                <div>10.[升级]JustAuth 至 1.15.8</div>
                <div>11.[升级]Dubbo 至 2.7.8</div>
                <div>12.[升级]Guava 至 30.0-jre</div>
                <div>13.[升级]Avue 至 2.7.0</div>
                <div>14.[优化]Swagger封装以支持Knife4j最新API</div>
                <div>15.[优化]引入Knife4j增强配置,生产环境将完全隔离文档访问</div>
                <div>16.[修复]未引入租户插件后,自定义类空指针的问题</div>
                <div>17.[删除]Zipkin模块,推荐使用官方独立模式运行服务</div>
              </el-collapse-item>
              <el-collapse-item title="2.6.1.RELEASE发布，增加全局上下文系统，增加用户平台拓展模块" name="18">
                <div>1.[升级]SpringBoot 至 2.1.17.RELEASE</div>
                <div>2.[升级]Mybatis-Plus 至 3.4.0</div>
                <div>3.[升级]Knife4j 至 2.0.5</div>
                <div>4.[升级]JJWT 至 0.11.2</div>
                <div>5.[升级]FastJson 至 1.2.74</div>
                <div>6.[新增]上下文核心包，优化全局上下文配置</div>
                <div>7.[新增]secure模块的basic认证功能</div>
                <div>8.[新增]用户平台拓展模块</div>
                <div>9.[优化]重构增强cloud模块</div>
                <div>10.[优化]request核心至boot模块</div>
                <div>11.[优化]增强mybatis-plus的分页防注入功能</div>
                <div>12.[优化]sms返回结果，去掉验证码序列化</div>
                <div>13.[优化]数据权限插件支持最新版mybatis-plus</div>
                <div>14.[优化]增强sql日志拦截器</div>
                <div>15.[优化]增强令牌，新增对用户平台的判断逻辑</div>
                <div>16.[优化]代码生成增加对sqlserver的支持</div>
                <div>17.[优化]自定义mapper的api</div>
                <div>18.[修复]Kv类克隆强转问题</div>
                <div>19.[修复]elk配置无法读取项目名的问题</div>
                <div>20.[修复]区划字段level为regionLevel以防oracle报错</div>
              </el-collapse-item>
              <el-collapse-item title="2.6.0.RELEASE发布，租户数据库隔离、报表管理、SqlServer兼容" name="17">
                <div>1.[升级]Avue 至 2.6.15</div>
                <div>2.[升级]SpringBoot 至 2.1.16.RELEASE</div>
                <div>3.[升级]Seata 至 1.3.0</div>
                <div>4.[升级]Nacos 至 1.3.2</div>
                <div>5.[升级]FastJson 至 1.2.73</div>
                <div>6.[升级]Knife4j 至 2.0.4</div>
                <div>7.[升级]EasyExcel 至 2.2.6</div>
                <div>8.[升级]JustAuth 至 1.15.6</div>
                <div>9.[新增]多租户数据库隔离、动态数据源特性</div>
                <div>10.[新增]SqlServer兼容</div>
                <div>11.[新增]UReport2报表管理模块</div>
                <div>12.[新增]对象存储附件表功能</div>
                <div>13.[优化]LocalFile支持序列化</div>
                <div>14.[优化]MinioTemplate增加ContentType配置</div>
                <div>15.[优化]LogBack-Elk的配置</div>
                <div>16.[优化]流程状态变更的返回信息</div>
                <div>17.[优化]顶部菜单配置接口，支持大容量数据传输</div>
                <div>18.[优化]User密码字段序列化</div>
                <div>19.[优化]序列化additionalInformation，解决非null值报错的问题</div>
                <div>20.[修复]启用Token有状态模式下刷新Token的问题</div>
                <div>21.[修复]日志表无法入库TenantId的问题</div>
                <div>22.[修复]flowable-oracle脚本运行错误的问题</div>
              </el-collapse-item>
              <el-collapse-item title="2.5.1.RELEASE发布，增加第三方登录、行政区划、API报文加密" name="16">
                <div>1.[升级]Avue 至 2.6.1、ElementUI 至 2.13.2</div>
                <div>2.[升级]SpringBoot 至 2.1.14.RELEASE</div>
                <div>3.[升级]SpringCloud 至 Greenwich.SR6</div>
                <div>4.[升级]SpringCloud Alibaba 至 2.1.2.RELEASE</div>
                <div>5.[升级]Seata 至 1.2.0</div>
                <div>6.[升级]FastJson 至 1.2.70</div>
                <div>7.[升级]Knife4j 至 2.0.3</div>
                <div>8.[升级]MybatisPlus 至3.3.2</div>
                <div>9.[升级]EasyExcel 至 2.2.4</div>
                <div>10.[新增]第三方系统登录，集成拓展JustAuth</div>
                <div>11.[新增]行政区划功能模块</div>
                <div>12.[新增]API报文加密工具</div>
                <div>13.[新增]Token配置，支持有状态模式，支持一人在线或多人在线</div>
                <div>14.[新增]Secure配置，支持配置请求方法类型、请求路径、请求表达式匹配</div>
                <div>15.[新增]Jackson配置，支持大数字转字符串模式，支持null转空值模式</div>
                <div>16.[新增]租户账号授权码保护机制，防止私有部署客户篡改数据库越权</div>
                <div>17.[优化]字典模块，增加树形结构</div>
                <div>18.[优化]新增租户逻辑，新增时同步超管配置的默认业务字典数据</div>
                <div>19.[优化]用户导入逻辑，只有超管才可以定义租户编号</div>
                <div>20.[优化]部门列表逻辑，非超管角色只可看到本级及以下部门数据</div>
                <div>21.[优化]字典模块，增加枚举类，统一入口</div>
                <div>22.[优化]DictCache缓存加载逻辑</div>
                <div>23.[优化]租户缓存刷新逻辑</div>
                <div>24.[优化]角色配置逻辑，同步取消子角色对应的菜单权限</div>
                <div>25.[优化]顶部菜单，增加排序功能</div>
                <div>26.[优化]INode，支持泛型</div>
                <div>27.[优化]代码结构，为bean统一加上final关键字修饰</div>
                <div>28.[优化]Nacos动态刷新配置</div>
                <div>29.[优化]Dockerfile，采用Openj9基础镜像，大幅度降低内存占用</div>
                <div>30.[优化]工程启动逻辑，关闭Flowable自动建表功能，需要手动导入流程sql</div>
                <div>31.[修复]SpringBootAdmin读取actuator路径配置</div>
                <div>32.[修复]用户导入逻辑，修正密码加密规则</div>
                <div>33.[修复]Boot版本Xss默认配置路径</div>
              </el-collapse-item>
              <el-collapse-item title="2.5.0.RELEASE发布，增加岗位管理，增加用户导入导出" name="15">
                <div>1.[升级]Avue 至 2.5.0</div>
                <div>2.[升级]SpringBoot 至 2.1.13</div>
                <div>3.[升级]FastJson 至 1.2.68</div>
                <div>4.[升级]Druid 至 1.1.22</div>
                <div>5.[升级]Knife4j 至 2.0.2</div>
                <div>6.[升级]Taobao-Sdk 至 20200415</div>
                <div>7.[升级]docker-maven-plugin 至 dockerfile-maven-plugin</div>
                <div>8.[新增]验证码开关</div>
                <div>9.[新增]数据权限全局开关</div>
                <div>10.[新增]岗位管理模块</div>
                <div>11.[新增]用户Excel导入导出功能</div>
                <div>12.[新增]用户绑定岗位功能</div>
                <div>13.[新增]EasyExcel封装工具ExcelUtil</div>
                <div>14.[新增]Feign内部线程传递</div>
                <div>15.[新增]Mybatis-Plus配置，支持配置最大分页数</div>
                <div>16.[新增]Gateway在多团队协作模式灵活指向本地服务的配置</div>
                <div>17.[新增]Sms模块的sendMessage接口及SmsResponse响应类</div>
                <div>18.[新增]CacheUtil租户缓存隔离功能</div>
                <div>19.[优化]CacheUtil缓存重载逻辑，返回bean不为null但数据全为空将不入缓存</div>
                <div>20.[优化]缓存清除逻辑，@CacheEvict统一修改为CacheUtil.clear</div>
                <div>21.[优化]登录逻辑，前端对密码加密后再传递至鉴权接口</div>
                <div>22.[优化]Oss上传接口，返回domain字段</div>
                <div>23.[优化]BladeRedisCache命名为BladeRedis</div>
                <div>24.[优化]控制台日志打印功能，规避MultipartFile读取报错</div>
                <div>25.[优化]配置关键字enable统一为enabled</div>
                <div>26.[优化]keyword日期处理</div>
                <div>27.[优化]代码生成sql脚本默认在工作台菜单下</div>
                <div>28.[优化]Jwt获取Token逻辑</div>
                <div>29.[优化]Token返回，增加岗位ID</div>
                <div>30.[优化]TokenGranter，采用更简洁的拓展方式</div>
                <div>31.[优化]日志管理展现方式</div>
                <div>32.[优化]新建租户逻辑，增加参数读取来设置新建租户的配置</div>
                <div>33.[优化]流程签收接口，支持多角色操作</div>
                <div>34.[优化]动态网关，支持读取自定义namespace配置</div>
                <div>35.[优化]删除租户逻辑，同时删除对应的用户</div>
                <div>36.[优化]树形懒加载，支持局部实时刷新功能</div>
                <div>37.[优化]多租户插件新增修改逻辑，若指定tenantId为空则不进行操作</div>
                <div>38.[优化]SmsBuilder、OssBuilder</div>
                <div>39.[优化]Sentinel配置</div>
                <div>40.[优化]XssFilter为全局的BladeRequestFilte</div>
                <div>41.[优化]BladeX开发手册Linux部署章节讲解</div>
                <div>42.[优化]Saber相关配置，以适配Avue最新版API</div>
                <div>43.[优化]Saber相关配置内done与loading的顺序</div>
                <div>44.[修复]用户基本信息修改的bug</div>
                <div>45.[修复]QiniuTemplate的putFile循环调用的bug</div>
                <div>46.[修复]日志框架获取RequestBody为空的bug</div>
                <div>47.[修复]Saber组件被复用导致没有刷新的bug</div>
                <div>48.[删除]过时的BladeSecureUrlProperties</div>
                <div>49.[删除]过时的XssUrlProperties</div>
                <div>50.[删除]过时的RedisUtil</div>
              </el-collapse-item>
              <el-collapse-item title="2.4.0.RELEASE发布，增加多租户短信服务，升级Seata1.1" name="14">
                <div>1.[新增]集成七牛、阿里云、腾讯云、云片等短信服务，支持多租户配置</div>
                <div>2.[新增]对象存储模块的资源编号字段，可根据编号指定oss配置的服务</div>
                <div>3.[新增]对象存储、短信配置模块的调试功能，可在线调试配置是否可用</div>
                <div>4.[新增]超管启用租户过滤的配置</div>
                <div>5.[升级]SpringBoot 2.1.12，SpringCloud SR5</div>
                <div>6.[升级]兼容 Seata 1.1</div>
                <div>7.[优化]对象存储的模块使用体验</div>
                <div>8.[优化]兼容Oracle模糊查询的写法</div>
                <div>9.[优化]超管权限，不受租户过期时间影响</div>
                <div>10.[优化]mybatis-plus相关过期注解</div>
                <div>11.[优化]xxl-job模块的配置文件</div>
                <div>12.[优化]INode支持序列化接口</div>
                <div>13.[优化]统一Oss模块命名</div>
                <div>14.[优化]部署脚本，升级相关版本</div>
                <div>15.[修复]数据权限部门过滤已删除对象</div>
                <div>16.[修复]业务字典缓存bug，增加租户过滤</div>
                <div>17.[修复]占位符解析器的bug</div>
              </el-collapse-item>
              <el-collapse-item title="2.3.1.RELEASE发布，流程增加租户定制，登录增加验证码" name="13">
                <div>1.[新增]登录验证码功能</div>
                <div>2.[新增]Oauth2自定义TokenGranter</div>
                <div>3.[新增]工作流绑定租户功能，支持通用流程和定制流程</div>
                <div>4.[新增]Condition类的自定义参数排除入口</div>
                <div>5.[增强]租户插件功能，新增操作可根据自定义的tenantId值进行覆盖</div>
                <div>6.[增强]超管权限，不受数据权限插件影响</div>
                <div>7.[升级]mybatis-plus至3.3.1</div>
                <div>8.[优化]mybatis-plus封装，提升分页可拓展性</div>
                <div>9.[优化]lib分离打包逻辑</div>
                <div>10.[优化]CacheUtil初始化逻辑</div>
                <div>11.[优化]HttpUtil，采用最新封装逻辑</div>
                <div>12.[优化]角色信息获取逻辑为实时，不受开源版、单体版缓存影响</div>
                <div>13.[优化]日志打印工具判断空逻辑</div>
                <div>14.[修复]BeanUtil的class类型判断逻辑</div>
                <div>15.[删除]基于zookeeper体验不佳的分布式锁</div>
              </el-collapse-item>
              <el-collapse-item title="2.3.0.RELEASE发布，租户增强，底层架构插件全面增强" name="12">
                <div>1.[新增]swagger-bootstrap-ui全新升级为knife4j</div>
                <div>2.[新增]saber升级至avue2.3.7版本</div>
                <div>3.[新增]saber树表懒加载模式</div>
                <div>4.[新增]腾讯云存储封装</div>
                <div>5.[新增]xxl-job集成，支持分布式任务调度</div>
                <div>6.[新增]kafka、rabbitmq、cloudstream集成</div>
                <div>7.[新增]redis分布式锁插件</div>
                <div>8.[新增]高性能http调用模块</div>
                <div>9.[新增]PropertySource注册逻辑，提高安全性</div>
                <div>10.[新增]Param参数缓存工具类</div>
                <div>11.[新增]租户操作，增加创建对应的租户管理员账号、菜单权限</div>
                <div>12.[新增]租户插件，超管可查看所有租户数据的逻辑</div>
                <div>13.[新增]租户功能，绑定域名、系统背景、账号额度、过期时间</div>
                <div>14.[新增]登录、创建用户操作绑定租户配置</div>
                <div>15.[优化]租户插件判断逻辑，增加flowable相关表的租户过滤排除</div>
                <div>16.[优化]xss过滤逻辑，提高性能</div>
                <div>17.[优化]本地文件上传逻辑</div>
                <div>18.[优化]oss配置，修改后及时生效无需点击启用</div>
                <div>19.[优化]请求日志展示功能</div>
                <div>20.[修复]前端关闭租户模式导致的新增用户失效问题</div>
                <div>21.[修复]OSS相关bucket命名的问题</div>
                <div>22.[修复]ribbon组件由降级引起的问题</div>
              </el-collapse-item>
              <el-collapse-item title="2.2.2.RELEASE发布，增强字典管理，用户管理增加左树右表" name="11">
                <div>1.[优化]拆分出系统字典表与业务字典表，字典键值改为string类型</div>
                <div>2.[优化]用户管理增加左树右表功能</div>
                <div>3.[优化]租户新增增加租户默认类型</div>
                <div>4.[优化]多租户表对应实体继承TenantEntity</div>
                <div>5.[优化]用于本地上传的BladeFile类更名为LocalFile防止冲突</div>
                <div>6.[优化]菜单新增逻辑</div>
                <div>7.[优化]mybatis-plus默认配置的处理</div>
                <div>8.[优化]租户过滤判断逻辑，删除多余的类</div>
                <div>9.[优化]alioss生成地址的逻辑</div>
                <div>10.[优化]redisTemplate加载逻辑</div>
                <div>11.[优化]租户处理，简化配置，自动识别需要过滤的租户表</div>
                <div>12.[优化]数据权限表单用户体验</div>
                <div>13.[修复]数据权限插件不兼容的问题</div>
                <div>14.[修复]数据权限树勾选显示问题</div>
                <div>15.[修复]windows平台elk开关失效的问题</div>
                <div>16.[修复]租户bean加载逻辑</div>
                <div>17.[修复]saber代码生成驼峰路径导致的问题</div>
                <div>18.[修复]docker脚本nginx端口匹配问题</div>
                <div>19.[修复]机构模块提交未删除缓存的问题</div>
                <div>20.[修复]oss缓存获取未加租户判断的问题</div>
                <div>21.[修复]blade-auth在java11下无法运行的问题</div>
              </el-collapse-item>
              <el-collapse-item title="2.2.1.RELEASE发布，集成ELK，增加分布式日志追踪" name="10">
                <div>1.[新增]集成最新版ELK，增加分布式日志追踪功能</div>
                <div>2.[新增]增加ELK一键部署docker脚本</div>
                <div>3.[新增]抽象封装日志管理逻辑</div>
                <div>4.[新增]BladeX-Biz增加easypoi的demo工程</div>
                <div>5.[新增]BladeX-Biz增加websocket的demo工程</div>
                <div>6.[优化]minio文件策略</div>
                <div>7.[新增]Sql条件构建类去除分页字段</div>
                <div>8.[优化]sql打印功能</div>
                <div>9.[优化]wrapper逻辑</div>
                <div>10.[新增]CommonConstant拆分出LauncherConstant</div>
              </el-collapse-item>
              <el-collapse-item title="2.2.0.RELEASE发布，增加集群监控，链路追踪" name="9">
                <div>1.[新增]turbine集群监控服务</div>
                <div>2.[新增]zipkin分布式链路追踪</div>
                <div>3.[升级]seata版本至0.9.0，解决分布式事务遇到的bug</div>
                <div>4.[新增]Launcher的nacos配置改为sharedIds，提升子工程配置优先级</div>
                <div>5.[新增]增加changeStatus方法，方便修改业务状态字段</div>
                <div>6.[新增]saber代码模板增加刷新事件</div>
                <div>7.[新增]saber底层架构升级</div>
                <div>8.[新增]saber支持tab切换保存页面状态</div>
                <div>9.[新增]添加bom统一版本配置</div>
                <div>10.[新增]添加trace starter</div>
                <div>11.[新增]blade-admin排除seata服务</div>
                <div>12.[新增]oss敏感操作增加权限校验</div>
                <div>13.[新增][修复]dict、role不选择父节点报错</div>
                <div>14.[新增]动态网关设置启动加载</div>
                <div>15.[新增]字典增加封存功能</div>
              </el-collapse-item>
              <el-collapse-item title="2.1.0.RELEASE发布，全面增强底层驱动" name="8">
                <div>1.[升级]springboot 2.1.8、springcloud greenwich sr3</div>
                <div>2.[新增]集成seata，提供最简集成方案</div>
                <div>3.[新增]blade-admin增加nacos动态监听</div>
                <div>4.[新增]增加alioss集成，强化oss返回信息</div>
                <div>5.[新增]获取令牌操作增加空判断</div>
                <div>6.[新增]拆分数据库依赖、增强mybatis、增加yml自定义配置读取</div>
                <div>7.[新增]各模块增加默认的yml配置，不占用application.yml</div>
                <div>8.[新增]增加ribbon组件，可自定义lb优先选择的ip段，解决团队网关调试需求</div>
                <div>9.[优化]feign的bean加载逻辑</div>
                <div>10.[增强]condition条件</div>
                <div>11.[优化]日志打印效果</div>
                <div>12.[重构]redis模块，增加redis限流功能</div>
                <div>13.[优化]beanutil性能</div>
                <div>14.[优化]去掉调试用的RouteEndpoint，增强安全性</div>
                <div>15.[优化]部门新增逻辑</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.7.RELEASE发布，增加网关鉴权，强化代码生成" name="7">
                <div>1.[新增]增加基于Nacos的动态网关鉴权</div>
                <div>2.[新增]代码生成增加多数据源选择，强化单表代码生成</div>
                <div>3.[新增]增加个人信息修改、头像上传、密码更新功能</div>
                <div>4.[优化]新建角色逻辑</div>
                <div>5.[修复]若干issue</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.6.RELEASE发布，兼容三大主流数据库" name="6">
                <div>1.[新增]一套代码兼容Mysql、Oracle、PostgreSQL三大主流数据库</div>
                <div>2.[升级]flowable 6.4.2</div>
                <div>3.[新增]超管默认拥有所有菜单权限</div>
                <div>4.[修复]权限配置数据长度过大的bug</div>
                <div>5.[新增]增加租户信息获取</div>
                <div>6.[优化]命令行启动顺序</div>
                <div>7.[升级]alibaba cloud毕业版本</div>
                <div>8.[新增]日志监听增加自定义配置</div>
                <div>9.[升级]swagger-bootstrap-ui版本</div>
                <div>10.[新增]saber表格自适应、增加loading</div>
                <div>11.[新增]saber通知公告模块增加富文本编辑器</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.5.RELEASE发布，升级分布式接口权限系统" name="5">
                <div>1.[升级]为分布式接口权限系统</div>
                <div>2.[新增]增加多租户自定义顶部菜单功能</div>
                <div>3.[升级]greenwich SR2，mybatis-plus 3.1.2</div>
                <div>4.[新增]swagger排序规则采用最新注解</div>
                <div>5.[新增]数据权限增加可见字段配置</div>
                <div>6.[新增]数据权限增加分布式服务支持</div>
                <div>7.[新增]增加远程调用分页的例子，解决mybatis-plus传递IPage反序化出现的bug</div>
                <div>8.[优化]租户接口权限规则</div>
                <div>9.[新增]SqlKeyword增加条件判断</div>
                <div>10.[修复]部分模块包名分层的问题</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.4.RELEASE发布，增加动态数据权限系统" name="4">
                <div>1.[新增]注解+web可视化配置的动态数据权限系统</div>
                <div>2.[升级]部门管理为机构管理，增加机构类型</div>
                <div>3.[新增]解决mybatis-plus排序字段的sql注入问题</div>
                <div>4.[新增]create_dept统一业务字段</div>
                <div>5.[新增]swagger ui页面设置Authorize 默认全局参数</div>
                <div>6.[新增]jsonutil增加封装方法,去掉devtools依赖</div>
                <div>7.[新增]数据库连接适配mysql8</div>
                <div>8.[新增]docker-compose脚本增加时区</div>
                <div>9.[新增]oauth申请token可支持自定义表</div>
                <div>10.[修复]代码生成sql缺失主键的问</div>
                <div>11.[新增]boot版本重构登录逻辑，增强可拓展性</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.3.RELEASE发布，优化多租户oss系统，优化业务架构" name="3">
                <div>1.[新增]gateway增加动态文档配置，可通过配置nacos动态刷新</div>
                <div>2.[优化]修正blade_menu代码生成模块删除api的地址</div>
                <div>3.[优化]mysql依赖</div>
                <div>4.[新增]LauncherService增加排序功能</div>
                <div>5.[优化]hystrixfeign加载</div>
                <div>6.[优化]多租户oss系统逻辑，使之更加易用</div>
                <div>7.tenant_code字段统一为tenant_id</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.2.RELEASE发布，增加多租户oss管理系统" name="2">
                <div>1.[新增]增加minio封装</div>
                <div>2.[新增]增加qiniu封装</div>
                <div>3.[新增]增加oss统一接口</div>
                <div>4.[新增]集成minio、qiniu，进行统一管理的多租户oss系统</div>
                <div>5.[优化]blade-core-cloud逻辑</div>
                <div>6.[新增]badex-biz增加不同包名的swagger、mybatis配置demo</div>
                <div>7.[新增]badex-biz增加nacos自定义注册文件demo</div>
                <div>8.[新增]bladex-biz增加nacos参数动态刷新demo</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.1.RELEASE发布，系统优化版本" name="1">
                <div>1.[新增]兼容jdk11</div>
                <div>2.[新增]支持refresh_token功能</div>
                <div>3.[新增]增加minio封装，支持多租户模式的oss对象存储</div>
                <div>4.[新增]集成dubbo最新版本，支持rpc远程调用</div>
                <div>5.[新增]定制基于nacos的gateway动态网关</div>
                <div>6.[优化]聚合网关配置，使之更加轻巧</div>
                <div>7.[新增]CacheUtil增加缓存清除方法</div>
                <div>8.[优化]日志文件格式</div>
                <div>9.[新增]Secure拦截器支持自定义加载</div>
              </el-collapse-item>
              <el-collapse-item title="2.0.0.RELEASE发布，完美定制的微服务开发平台" name="0">
                <div>1.[新增]Swagger提供list形式配置扫描包</div>
                <div>2.[新增]DictCache、UserCache、SysCache缓存工具类</div>
                <div>3.[新增]重新设计EntityWrapper结构，使之更加简单易用</div>
                <div>4.[新增]强化部分敏感数据的删除校验</div>
                <div>5.[新增]Condition类的sql条件构造器</div>
                <div>6.[修复]工作流分页bug</div>
                <div>7.[优化]docker配置</div>
                <div>8.[优化]多租户逻辑</div>
                <div>9.[优化]request打印日志逻辑</div>
                <div>10.[修复]getIp的bug</div>
                <div>11.[优化]saber代码生成模板</div>
                <div>12.[新增]saber更新至element-ui 2.8.2版本</div>
                <div>13.[修复]saber分页bug</div>
                <div>14.[新增]crud组件提交报错后恢复按钮状态</div>
                <div>15.[新增]字典管理表单调整</div>
                <div>16.[升级]springboot 2.1.5</div>
              </el-collapse-item>
            </el-collapse>
          </basic-container>
        </el-row>

      </el-col>
    </el-row>
  </div>
</template>

<script>
  import {mapGetters} from "vuex";

  export default {
    name: "wel",
    data() {
      return {
        activeNames: ['1', '2', '3', '5'],
        logActiveNames: ['23']
      };
    },
    computed: {
      ...mapGetters(["userInfo"]),
    },
    methods: {
      handleChange(val) {
        window.console.log(val);
      }
    },
  };
</script>

<style>
  .el-font-size {
    font-size: 14px;
  }
</style>

