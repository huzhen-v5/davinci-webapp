# Davinci Web Application

Davinci 是一个 DVaaS（Data Visualization as a Service）平台解决方案，面向业务人员/数据工程师/数据分析师/数据科学家，致力于提供一站式数据可视化解决方案。

Davinci源码地址：
[https://github.com/edp963/davinci](https://github.com/edp963/davinci)

Davinci源码大概分为三部分：
* 采用React的前端工程
* 采用Spring Boot的后端工程
* 采用Jekyll + Minmal Mistakes的文档工程，用来介绍Davinci的用户操作方法

> 笔者环境：<br>
> 系统：Windows10 64位<br>
> node版本：v12.13.1<br>
> npm版本：6.12.1<br>

前端部分代码在Davinci源码根目录的 `webapp/` 目录中

### 目录结构
```
├── app              # 主应用源码
  ├── assets           # 资源文件
  ├── components       # 通用组件
  ├── containers       # 路由容器组件
  ├── utils            # 通用实用方法
  └── app.tsx          # 主应用入口
├── internals        # 开发工程文件
├── libs             # 改动后的项目依赖
├── server           # 开发服务器
├── share            # 分享页源码
└── package.json
```
### 开发环境

建议：
* `node`： ">=8.10.0"
* `npm`： ">=5"


### 安装依赖
```
npm install
```

### 开发
```
npm start
```

### Lint
```
npm run lint
```

### Test
```
npm run test
```

### 打包
```
npm run build
```
### 常见问题
* `npm install`执行过程中报错：npm ERR! Unexpected end of JSON input while parsing near 'xxx'

    解决办法：<br>
    删除掉已经自动生成的`node_module`文件夹，然后再运行如下命令
    ```
    npm cache clean --force
    npm install    
    ```
* `npm install`执行过程中报错：`Error: Command failed: C:\WINDOWS\system32\cmd.exe /s /c `，或者报错：`Error: pngquant failed to build, make sure that libpng-dev is installed`
  
    解决办法：<br>
	换个网络环境重新执行`npm install`，确保网络能够访问到`npm`源和`git`源
	
* `npm start`执行完后，可以正常访问登陆页面，但是控制台提示很多类似`TS232`的错误

    解决办法：<br>
    这个可能是源码中的TypeScript语法不规范引起的，笔者将在后面尝试修复这些错误，这些错误不影响正常开发，可以忽略

### 更多关于`Davinci`的文章，可以看笔者的CSDN专栏
[https://blog.csdn.net/huzhenv5/category_9690864.html](https://blog.csdn.net/huzhenv5/category_9690864.html)