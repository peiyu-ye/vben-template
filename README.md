## 介绍

该项目为 [vue-vben-admin2.0](https://github.com/anncwb/vue-vben-admin)的精简版本。

## 环境要求

- Node.js: - 版本最好大于 12.0.0
- 包管理工具: yarn > npm > cnpm

### 精简版地址

[vue-vben-admin-thin-next](https://github.com/anncwb/vben-admin-thin-next)

## 预览地址

- [2.0 精简版 在线预览](https://vvbin.cn/thin/next/)

## 修改清单

当你开始使用时，请按下面列表先行修改项目

- [ ] 重命名 `package.json` 中的 `name` 字段
- [ ] 在`LICENSE`中更改作者姓名
- [ ] 在`public`中修改 `favicon.ico`
- [ ] 在`public/resource/`和`/src/assets/images/logo.png`中修改 `logo.png`
- [ ] 在`.env[xxx]`文件中修改相关项目配置
- [ ] 在`src/settings/projectSetting.ts`内调整适合自己的项目风格
- [ ] 项目默认启用角色来控制菜单，且后台请求菜单已被注释，如果需要使用后台动态生成路由。请将`/src/store/modules/permission.ts`内的关于动态请求菜单的注释放开

## 注意

依赖删除了`echarts`,`apexcharts`,`zxcvbn`,`qrcode`四个模块。但是组件及代码未删除。在你未引用到相关组件的时候，不会发出错误。当你需要使用的时候，只需要执行相应的命令安装对应模块即可

需要用到哪个则执行对应命令

```js
// echarts 需要单独在 vite.config.ts内加上
// optimizeDeps: {
//     include: [
//       'echarts',
//     ],
//   },
yarn add echarts

yarn add apexcharts

yarn add zxcvbn

yarn add qrcode

```

### 开发环境

```bash
yarn serve
```

### 打包

```bash

yarn build # 打包

yarn build:no-cache # 打包，执行之前会先删除缓存

yarn report # 生成构建包报表预览
```

### 格式化

```bash
yarn lint:stylelint # 样式格式化

yarn lint:prettier # js/ts代码格式化
```

### 其他

```bash
yarn reinstall # 删除依赖重新装，兼容window

yarn preview # 本地进行打包预览

yarn log # 生成CHANGELOG

yarn clean:cache # 删除缓存

yarn clean:lib # 删除node_modules，兼容window系统
```
