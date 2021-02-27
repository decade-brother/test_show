---
title: node中模块的加载机制
---

## 模块的缓存机制

 - 模块在第一次加载后会被缓存, 如果每次调用相同模块都解析到同一文件，则返回相同的对象,不会导致模块的代码被执行多次


## 内置模块的加载机制

 - 在存在相同名称的时候，会优先加载内置模块


## 自定义模块的加载机制

 - 在引入自定义文件模块时，如果路径后带后缀，就会加载指定文件，如果不加后缀名，加载顺序为.js => .json => node => 报错

 - 在引入自定义目录模块时，会先找目录下的package.json文件，然后在该文件中查找main属性对应的主入口，如果没有就找index.js文件 ，再没有就报错

## 第三方模块的加载机制

 - 在查找文件的时候根据module.paths属性数组中的路径，由内向外查找，保持就近原则；以下为作者在自己电脑上输出module.paths的属性值，仅供参考

  ```js
  [
    'C:\\Users\\mxs\\Desktop\\node\\lesson003\\04-第三方模块的加载机制\\node_modules',
    'C:\\Users\\mxs\\Desktop\\node\\lesson003\\node_modules',
    'C:\\Users\\mxs\\Desktop\\node\\node_modules',
    'C:\\Users\\mxs\\Desktop\\node_modules',
    'C:\\Users\\mxs\\node_modules',
    'C:\\Users\\node_modules',
    'C:\\node_modules'
  ]
  ```

  