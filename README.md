# 简介

这个是一个 cocos creator 工程侧的模版，里面集成了 git 规范,lint 规范, 目录规范, 构建,工程侧提供的核心模块: dino-core, stt, sladar, util-http, 同时会集合一些常用的游戏组件, 大大提高游戏开发效率，保证游戏项目的稳定

# 项目基本结构

项目的基本结构如下:

```
assets
├─texture
|    ├─view
|    ├─list
|    ├─item
|    ├─dialog
|    ├─common
├─script
|   ├─app.ts
|   ├─utils.ts
|   ├─model
|   ├─config
|   |   ├─config.common.ts
|   |   ├─config.develop.ts
|   |   ├─config.local.ts
|   |   ├─config.prod.ts
|   ├─components
|   |     ├─view
|   |     ├─list
|   |     ├─item
|   |     ├─dialog
|   ├─api
├─scene
|   ├─index.fire
├─resources
|     ├─texture
|     |    ├─view
|     |    ├─list
|     |    ├─item
|     |    ├─dialog
|     |    ├─common
|     ├─spine
|     ├─prefab
|     |   ├─view
|     |   ├─list
|     |   ├─item
|     |   ├─dialog
|     |   ├─common
|     ├─dragonbones
├─prefab
|   ├─view
|   ├─list
|   ├─item
|   ├─dialog
|   ├─common
├─build_config
|      ├─develop.env
|      ├─local.env
|      ├─product.env
```

整体目录结构说明如下:

- app.ts 是整个工程启动的入口文件, 默认场景必须挂载 app.ts 组件。
- model 目录是游戏的模型对象
- config 是游戏项目的配置文件, 文件命名: config.xxx.ts
- components 目录是游戏项目的逻辑业务组件
- api 目录是存放所有游戏项目的请求 api
- view、dialog、common、list、item 是资源分类目录, 属于对应的资源放置进去对应的目录即可

# 模型管理

游戏的模型管理主要通过 dino-core 提供的模型管理能力，具体使用可以参考[dino-core 使用文档](https://bytedance.feishu.cn/docs/doccn0GWMxAFSu3laEHR2r0Elsc)

# stt

stt 是对头条小游戏 tt 的封装, 主要有如下特点:

- 接口 promisify 化
- 修复一些 tt 提供能力 sdk 版本的 bug

具体使用可以参考[stt 使用文档](https://bytedance.feishu.cn/docs/doccnvAKLvyjI1G60e30dDbDkrd)

# 网络请求

网络请求提供了请求的基本能力, 主要有如下特点:

- 文件上传封装
- 文件下载封装
- 请求失败成功错误监控

具体使用可以参考[util-http 使用文档](https://bytedance.feishu.cn/docs/doccn1FJOahw7OCk72YFsHTzoVb#RwSToc)

# 日志上报

日志上报使用的是 sladar 服务, 使用可以参考[sladar 使用参考](https://bytedance.feishu.cn/docs/doccndRI6DYjGIyDF5tW2KTnrqg#)

# 构建

构建分为本地、头条小游戏 IDE、正式服三种环境。构建的配置在 build_config 目录下面。

## 本地构建

```
npm run local
```

## IDE 构建

```
npm run dev
```

## 正式服构建

```
npm run prod
```

## 自动化构建

工程提供了自动化构建的能力, 具体使用参考[自动化构建使用说明](https://bytedance.feishu.cn/docs/doccnPESA8EpoNaxDdsyZj4NcUc)

构建配置参数填写可以参考[构建配置使用](https://bytedance.feishu.cn/docs/doccn5kHSE5x54f42EpLkgaJhhn)

# 游戏组件

cocos template 为游戏提供了常用的游戏组件，具体使用可以参考[游戏组件使用](https://bytedance.feishu.cn/docs/doccnZMlqfeNroB5Zwg3SowUwld)
