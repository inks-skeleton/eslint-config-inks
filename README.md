# Eslint + Prettier
> `eslint-config-inks` 是为 `inks-skeleton` 框架定制的代码规范，按照指南按照可进行保存按eslint规则自动格式化，prettier规则美化代码。代码仓库：
[Github](https://github.com/inks-skeleton/eslint-config-inks)
[Gitee](https://gitee.com/inks-skeleton/eslint-config-inks)

## 安装指南

- 快速安装：
  ```
  npm install eslint-config-inks -D
  ```

- 安装最新版本：
  ```
  npm install eslint-config-inks@latest -D
  ```

- 安装指定版本：
  ```
  npm install eslint-config-inks@1.0.0 -D
  ```

- 本地调试：
  ```
  // 创建全局link，进入npm模块项目目录
  cd eslint-config-inks
  npm link

  // 进入需要使用npm模块的项目目录
  cd my-app
  npm link eslint-config-inks

  // 解除全局link，进入npm模块项目目录
  cd eslint-config-inks
  npm unlink
  ```


## 使用说明

**1. 在项目根目录创建 ``.eslintrc.js``**
**2. 复制下列你需要的内容版本至文件中：**
- 通用项目
  ```
  module.exports = {
    root: true,
    extends: ['eslint-config-inks' ]
  }
  ```

- 微信小程序项目
  ```
  module.exports = {
    root: true,
    extends: [ 'eslint-config-inks' ],
    globals: {
      __DEV__: true,
      __WECHAT__: true,
      __ALIPAY__: true,
      App: true,
      Page: true,
      Component: true,
      Behavior: true,
      wx: true,
      getApp: true,
      getCurrentPages: true
    }
  }
  ```

**3. 对应安装以下依赖库：**
- 通用项目
  ```
  npm install babel-eslint@10.1.0 eslint@6.7.2 eslint-plugin-prettier@3.3.1 eslint-plugin-vue@6.2.2 prettier@2.2.1 -D
  ```
  依赖列表：
  - ``babel-eslint@10.1.0``
  - ``eslint@6.7.2``
  - ``eslint-plugin-prettier@3.3.1``
  - ``eslint-plugin-vue@6.2.2``
  - ``prettier@2.2.1``

- vue-cli创建的项目
  ```
  npm install @vue/cli-plugin-eslint@4.5.0 @vue/cli-plugin-babel@4.5.0 @vue/eslint-config-prettier@4.5.0
  ```
  依赖列表：
  - ``@vue/cli-plugin-eslint@4.5.0``
  - ``@vue/cli-plugin-babel@4.5.0``
  - ``@vue/eslint-config-prettier@4.5.0``


> 以上依赖库，跨度过大的版本会有兼容问题，如非必须建议使用提供的版本进行安装

> 特殊说明：当前eslint 8.* 与 @vue/cli-plugin-eslint@4.* 存在冲突情况，会报错

**4. 配置对应的编辑器，如需按照插件的，请自行安装，并配置启用Eslint + Prettier**
