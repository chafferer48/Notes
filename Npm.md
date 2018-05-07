## NPM 笔记

### 参考：

[NPM官网](https://docs.npmjs.com/getting-started/updating-local-packages) ：https://docs.npmjs.com/getting-started/updating-local-packages

[package.json入门教程](https://blog.csdn.net/u011240877/article/details/76582670) : https://blog.csdn.net/u011240877/article/details/76582670

### NPM 常用命令

```
更新npm：      npm install npm@latest -g

更新某个依赖包：npm update <package-name>

更新全部依赖包：npm update

可更新依赖包：  npm outdated
```

### package.json 说明

```
出现package.json：npm init    npm init --yes 跳过回答问题，直接出现package.json文件

语义化版本规则：

    1. dependencies：生产需要的依赖

    2. devDependencies：开发需要的依赖

    3. 升级版本需要遵循的版本规则：

        + 补丁版本：解决了 Bug 或者一些较小的更改，增加最后一位数字，比如 1.0.1

        + 小版本：增加了新特性，同时不会影响之前的版本，增加中间一位数字，比如 1.1.0

        + 大版本：大改版，无法兼容之前的，增加第一位数字，比如 2.0.0

    4. npm依赖包的版本规则

        + 如果只打算接受补丁版本的更新（也就是最后一位的改变），就可以这么写： 
            1.0
            1.0.x
            ~1.0.4

        + 如果接受小版本的更新（第二位的改变），就可以这么写： 
            1
            1.x
            ^1.0.4

        + 如果可以接受大版本的更新（自然接受小版本和补丁版本的改变），就可以这么写： 
            *
            x
            
    5. 安装依赖参数

        + npm install <package_name> --save 表示将这个包名及对应的版本添加到 package.json的 dependencies 

        + npm install <package_name> --save-dev 表示将这个包名及对应的版本添加到 package.json的 devDependencies
```

