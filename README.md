# demo

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### 环境安装
```
全局安装vue-cli

npm install -g @vue/cli
创建uni-app
使用正式版（对应HBuilderX最新正式版）

vue create -p dcloudio/uni-preset-vue my-project
使用alpha版（对应HBuilderX最新alpha版）

vue create -p dcloudio/uni-preset-vue#alpha my-alpha-project


运行、发布uni-app
npm run dev:%PLATFORM%
npm run build:%PLATFORM%

app-plus	app平台生成打包资源（支持npm run build:app-plus，可用于持续集成。不支持run，运行调试仍需在HBuilderX中操作）
h5	H5
mp-alipay	支付宝小程序
mp-baidu	百度小程序
mp-weixin	微信小程序
mp-toutiao	字节跳动小程序
mp-qq	qq 小程序
mp-360	360 小程序
quickapp-webview	快应用(webview)
quickapp-webview-union	快应用联盟
quickapp-webview-huawei	快应用华为

```

### uView使用

```
// 安装
yarn add uview-ui

// 更新
yarn update uview-ui

// 安装其他
yarn add sass sass-loader@10.1.1 node-sass  -D
```