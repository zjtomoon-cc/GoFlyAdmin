# GoFly快速开发后台管理系统介绍
## 一、框架介绍
框架采用前后端分离，将Go与Vue结合开发中后台系统，Go作为一种高效、安全的编程语言，可以帮助开发者快速构建高效、可靠、安全的应用，Vue作为前端优秀框架，可以快速搭建漂亮，高体验，稳定前端页面。能让开发者开发时顺手，客户使用时满意，性能与颜值并存，让开每一个项目交付都能让您和您的客户双方都满意。Go 开发业务接口，vue 开发前端界面。后台管理系统从业务上分为：
总管理系统（admin 端简称 A 端）和业务端管理系统（专门编写业务的，方便系统做出 saas 形系统，
减少后期需要多个应用重构成本，遇到买系统时不要单独重新部署直接再 A 端开一个账号就可以，
业务端 business 简称 B 端）。天生自带SAAS多账号数据分离，可以做到不用重新部署，即可单独拉出新的一套。

GoFly快速开发框架来自我们的医疗项目，从2019年开始用于医疗系统开发，医疗项目已经运行多年，框架的安全性、并发性能、稳定性已经得到验证。特别是在疫情期间的疫苗预约接种留观等并发和反应速度都表现良好,你可放心使用于你的项目中去。

框架采用前后端分离，Go开发使用热编译，开发目录不建议太多文件，影响编译扫描效率，前段建议放在另外位置，
git上传了全部的Go源码，前端代码和数据库请到[GoFly社区下载](https://goflys.cn/prdetail?id=6)，使用时有问题请加技术客服咨询，我们社区的初心是为不让开发者为难，打造一个让大家都舒服的社区，与大家共建一个伟大的社区。

如果您觉得好，请您帮忙宣传，给GoFly作者们点个⭐️star吧！让更多人使用，让Go火起来，大家都好找工作，企业可以降低成本，为企业个人降本增效！
## 二、优势简介
1. 基于优秀成熟框架集成，保证系统可靠性。集成的主要有 Gin、Arco Design 、Mysql 等主流框架技术。

2. 系统已集成开发常用基础功能，开箱即用，快速开始您业务开发，快人一步，比同行节省成本，降本增效首选。

3. 框架提供其他开发者开发的插件，可快速安装或卸载，让开个资源共享，同意功能无需重复造车，一键安装即可使用。 框架搭建了一键 CRUD 生成前后端代码，建数据库一键生成，节省您的复制粘贴时间，进一步为您节省时间。

4. 框架自带 API 接口文档管理，接口带有请求 token 等配置，添加接口只需配置路径和数据库或者备注，其部分信息如数据字段，系统自动根据数据库字段补齐，开发配套接口文档尽可能的为您节省一点时间。不需要其他接口文档工具复制粘贴，登录注册等时间。还有一个重点！接口文档可以一键生成接口 CRUD 的代码和通用的操作数据的 CRUD 接口，根据您的业务选择自己写接口代码、一键生成接口代码、不用写和生成代码调用通用接口。让写接口工作节省更多时间。

5. 前后端分离解耦业务，让前段人员与后端人协调开发，提高项目交付，并且可以开发出功能复杂度高的项目。

6. 前端用 Vue3+TypeScript 的 UI 框架 [Arco Design](https://arco.design/vue/component/button)，好用的 UI 框架前端可以设计出优秀且交互不错的界面，完善的大厂 UI 支持，前端开发效率也很高！ 以上只是框架比较明显优势点，还有很多优势等你自己体验，我们从各个开发环节，努力为您节省每一分时间。
7. 集成操作简单的 ORM 框架，操作数据非常简单，就像使用 thinkphp 一样，您可以去文档看看 [框架的ROM数据库操作文档](https://doc.goflys.cn/docview?id=25&fid=289)
   例如下面语句就可以查找一条数据：
 ```
  db.Table("users").Fields("uid,name,age").First()
```
## 三、目录结构

```
├── app                     # 应用目录
│   ├── admin               # 后台管理应用模块
│   ├── business            # 业务端应用模块
│   ├── common              # 公共应用模块
│   ├── home                # 可以编写平台对应网站
│   ├── wxapp               # 微信小程序模块
│   ├── wxoffi              # 微信公众号模块
│   └── controller.go       # 应用控制器
├── bootstrap               # 工具方法
├── config                  # 配置文件
├── global                  # 全局变量
├── model                   # 数据模型
├── resource                # 静态资源
├── route                   # 路由
├── runtime                 # 运行日志文件
├── tmp                     # 开发是使用fresh热编译 产生临时文件
├── utils                   # 工具包
├── go.mod                  # 依赖包管理工具
├── go.sum         
├── main.go                 # main函数        
└── README.md               # 项目介绍
```
开发时仅需在app目录下添加你新的需求，app外部文件建议不要改动，除了config配置需要改，其他不要修改，
框架已经为您封装好，你只需在app应用目录书写你的业务，路由、访问权限、跨域、限流、Token验证、ORM等
框架已集成好，开发只需添加新的方法或者新增一个文件即可。
## 四、在线预览
 [1.GoFly全栈开发社区了解更多](https://goflys.cn/home)  

 [2.Go快速后台系统开发框架完整代码包下载](https://goflys.cn/prdetail?id=6)

 [3.Go快速后台系统开发文档](https://doc.goflys.cn/docview?id=25)

 [4.A端在线预览](https://sg.goflys.cn/webadmin)

 [5.B端在线预览](https://sg.goflys.cn/webbusiness)

## 五、效果图片预览
1.登录
![登录](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230507/f7c95d545b8c6b2efcdc67411717dff9.png?_t=1683391696?_t=1683391957?_t=1683392586?_t=1683392719?_t=1683431653?_t=1683457525?_t=1683788194?_t=1683900699?_t=1683900728?_t=1684131551?_t=1684131610?_t=1684248566?_t=1684251100?_t=1684251116?_t=1684942532?_t=1690089174?_t=1690381209?_t=1690381302?_t=1690381509?_t=1690381580?_t=1690384672?_t=1690384708?_t=1690417520?_t=1690615914?_t=1690616150?_t=1690616188?_t=1690616229?_t=1690616269?_t=1690616688?_t=1690616712?_t=1690619741?_t=1690621677?_t=1690622192?_t=1690622941?_t=1690654664?_t=1690654946?_t=1690696591?_t=1690907888?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
2.统计页
![统计页](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230808/b8304ca001cda4a94b86dad216ca5219.png?_t=1691428085)
3.角色管理-auth权限
![ 角色管理-auth权限](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/c4de74ba182c5037a4fd0390fb7a6ecf.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
4.数据中心-数据字典
![数据中心-数据字典](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/f894c904f617b32a8da0bb5310ed95e0.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
5. 数据中心-附件管理
![附件管理列表](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/c54d9d9141bad3aaa5a4923e7abcc32e.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
![附件管理器](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/23ec93d6787bfcbca2e6c930213671bd.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
6.数据中心-配置
![配置](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/fba8e679546d1f3fe450b94e7f239a51.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
7.微信业务
![微信菜单](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/79770e6d1fb7e4155c67f6637a4a33df.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
8.api接口管理
![api接口管理列表及测试接口](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/10132ac752b08efd8b2b2c56c6492775.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
![api接口管理添加接口](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/595c0301371762910ea3c20c1ce737ca.png?_t=1690908276?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158)
9.1 代码一键生成后端CRUD和前端代码
![代码一键生成后端CRUD和前端代码列表](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230808/0708c3ad360324d3af90ebebbf47db67.png?_t=1691428879)
![代码一键生成后端CRUD和前端代码添加](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/e2300484772ab8eb9bbf94a1d4503735.png?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158?_t=1691428879)
9.12 代码生成示例
![生成列表](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230808/23d844127703ba85731097a305571b89.png?_t=1691428879)
![生成添加表单](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/2622a5071f8f512e8f0a31e23990da3c.png?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158?_t=1691428879)
![生成添加表单-文本编辑器](https://admin.goflys.cn/common/uploadfile/get_image?url=resource/uploads/20230802/85c36eef5e37779858f2e912885f71c5.png?_t=1690908444?_t=1690908471?_t=1690908494?_t=1690908849?_t=1691152158?_t=1691428879)

## 六、GoFly SAAS开始开发后台系统-服务端
版本：v1.1.0

### 安装fresh 热更新-边开发边编译
go install github.com/pilu/fresh@latest
```
#请修改fresh配置runner.conf.sample中的 
ignored:           assets, tmp, web
添加 web 让他不要监听前端开发更新

```
### 初始化mod
go mod tidy

### 热编译运行
bee run 或 fresh 
### 打包
go build main.go
### 打包（此时会打包成Linux上可运行的二进制文件，不带后缀名的文件）
```
SET GOOS=linux
SET GOARCH=amd64
go build
```
### widows
```
// 配置环境变量
SET CGO_ENABLED=1
SET GOOS=windows
SET GOARCH=amd64

go build main.go

// 编译命令
```
### 编译成Linux环境可执行文件
```

// 配置参数
SET CGO_ENABLED=0 
SET GOOS=linux 
SET GOARCH=amd64 

go build main.go

// 编译命令
```

## 七、前端代码
由于前端后端分类，在Go本地开发使用fresh热编译，Go目录不能用太多文件影响编译时间，
所以我们开发是建议前端代码放在其他位置。然后再Go项目config/settings.yml配置文件中vueobjroot配置前端业务端开发路径：
```
vueobjroot: D:/Project/develop/vue/gofly_base/gofly_business
```
所以如果您使用GoFly快速框架开发项目，请您移步到[GoFly全栈开发社区下载完整包](https://goflys.cn/prdetail?id=6)
