# lit-ncov-report
洛阳理工学院 "健康状况管控平台" 的一个非官方`Python封装库`兼`CLI工具`与`拓展实现` (for severless)

[![pypi version](https://img.shields.io/pypi/v/litncov)](https://pypi.org/project/litncov/)
[![pypi downloads per month](https://img.shields.io/pypi/dm/litncov)](https://pypi.org/project/litncov/)
[![Docker Pulls](https://img.shields.io/docker/pulls/icepie/litncov.svg)](https://hub.docker.com/r/icepie/litncov/)
[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

[![QQ Group](https://img.shields.io/badge/QQ%20Group-768887710-red.svg)](https://jq.qq.com/?_wv=1027&k=lz0XyN86)
[![TG Group](https://img.shields.io/badge/TG%20Group-lit_edu-blue.svg)](https://t.me/lit_edu)

## 打包与部署

### 腾讯云SCF

在**云函数控制台-新建-自定义模板**

#### 函数代码

1. 在此 [releases](https://github.com/icepie/lit-ncov-report/releases/tag/lit-ncov-report-scf) 下载最新自动打包的版本

2. 然后在**提交方法**, 中选择**本地上传zip包**的方式

3. 在**执行方法**, 中使用 `index.main_handler` (一般默认就)

3. 点击选择好文件即可

#### 高级配置

- 选中**固定出口IP** (推送服务正常工作的必要选项)

- **执行超时时间** 设置为**900秒**

### 触发器配置

**自定义创建-定时触发-自定义触发周期**

```js
# 例如每日 6点, 12点, 20点进行轮询上报
0 0 6,12,20 * * * *
```

### 程序配置

在完成上诉操作后, 点击完成, 接下来打开**函数代码**进行配置

#### 基本配置

在`src/conf/conf.json`当中

请自行查看并编辑

#### 用户配置

在`src/conf/users,csv`当中

请自行添加~

### 最后

点击部署, 再测试一下就没问题啦

望使用愉快, 欢迎fork修改


### 阿里云SCF
请自行研究 :)
