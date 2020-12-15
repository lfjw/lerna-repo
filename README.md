# lerna 管理开源前端项目

## 常用命令

### 初始一个多包的工程

```sh
lerna init
```

上述命令会初始化一个多包工程。初始化之后会在根目录生成 packages 目录、lerna.json，如果使用 independent 模式，请使用命令：lerna init --independent

### 创建子包

```sh
lerna create <package> [-y]
```

在 packages 所指目录下创建 package 包。

### 添加包

```sh
lerna add <package>[@version] [--dev] [--exact] [--scope=module名]
```

上述命令会添加一个包 package 指明的软件包。

指定--dev 是添加在 devDependencies 中。

指定--exact，则将用精确匹配的版本添加包。

指定--scope 将只在此指明的模块中安装这个软件包，否则将在所有 packages 目录中的包中安装。

对于 packages 目录下的子包，将通过设立 systemlink 来解决依赖。

对于 npm 镜像中存在的包，将安装镜像中的包。
