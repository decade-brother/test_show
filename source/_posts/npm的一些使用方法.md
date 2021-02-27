---
title: npm的指令用法
---

## npm指令

### 初始化
```js
npm init -y //用来创建package.json文件
```


### 下载包
```js
npm install 包名 / npm i 包名
```


### 查看包
```js
npm view 包名
```


### 下载指定版本包
```js
npm i 包名@版本号
```

### package.json
```js
 一、package.json 配置文件中有两个关键的配置项: 
      
      1. dependencies: 在生产环境中所需要的软件包
      2. devDependencies: 仅本地开发和测试所需要的软件包

    二、上述配置项的作用
      其他项目成员在执行 `npm install` 命令时，会自动根据 package.json 文件中记录的包名称和版本信息
    全部进行下载
```
   

### 下载依赖(dependencies)里的所有包
```js
npm i
```

### 卸载指定包
```js
npm uninstall 包名
```

### 使用nrm切换源
```js
 - 1.先在全局下载nrm
    npm i -g nrm
 - 2.查看目前使用的源
    npm ls
 - 3.切换源
    npm use 源名
```


### 在终端登录npm账号
```js
npm login
```


### 在终端发布包
```js
npm publish 
```


### 在终端删除包
```js
npm unpublish 包名 --force
```
