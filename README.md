# 微应用运行时文档

## 简介

## 支持的平台

- Windows
- Mac OS
- Linux
- Android
- IOS
- 浏览器（需要支持 Canvas 和 Webassembly）

## 架构图

## JavaScript 引擎

JavaScript 引擎使用 QuickJS。

### 支持的 JavaScript 版本

> It supports the ES2020 specification including modules, asynchronous generators, proxies and BigInt.

支持 ES2020 特性，包括模块导入、异步生成器、proxies、大整型

### 性能基准

| 引擎                | QuickJS | DukTape | XS   | MuJS | JerryScript | Hermes | V8 (不使用 JIT) | V8 (JIT) |
| ------------------- | ------- | ------- | ---- | ---- | ----------- | ------ | --------------- | -------- |
| 可执行文件大小      | 620K    | 331K    | 1.2M | 244K | 211K        | 27M    | 28M             | 28M      |
| Richards            | 777     | 218     | 444  | 187  | 238         | 818    | 1036            | 29745    |
| DeltaBlue           | 761     | 266     | 553  | 245  | 255         | 1090   | 884             | 34215    |
| RayTrace            | 915     | 484     | 1156 | 392  | 286         | 937    | 2989            | 69781    |
| EarleyBoyer         | 1417    | 620     | 1175 | 315  | -           | 1728   | 4583            | 48254    |
| RegExp              | 251     | 156     | -    | 155  | -           | 335    | 2142            | 7637     |
| Splay               | 1641    | 1389    | 1048 | 36.7 | -           | 1602   | 4303            | 26150    |
| NavierStokes        | 1856    | 1003    | 836  | 109  | 394         | 1522   | 1377            | 36766    |
| 总分数 (w/o RegExp) | 1138    | 468     | 738  | 159  | -           | 1127   | 1886            | 41576    |
| 总分数              | 942     | 408     | -    | 158  | -           | 968    | 1916            | 33640    |

(分数越高越好).

[参考](https://bellard.org/quickjs/bench.html)

## UI 库

TODO

## API

- 文件读写
- 嵌入式数据库
- 网络
- 蓝牙
- 陀螺仪
- 媒体库

## 开发工具链

### 包管理器

使用 yarn？

### 打包工具

- babel?
- webpack?

## TODO 列表

- [ ] 选择 UI 库
- [ ] 集成 libuv
- [ ] 集成 curl
- [ ] 集成 SQLite3

## 使用的开源库

| 名称    | 许可证         | 项目主页                     |
| ------- | -------------- | ---------------------------- |
| QuickJS | MIT 许可证     | https://bellard.org/quickjs/ |
| libuv   | MIT 许可证     | https://libuv.org            |
| curl    |                |                              |
| SQLite3 | SQLite3 许可证 | https://www.sqlite.org/      |
