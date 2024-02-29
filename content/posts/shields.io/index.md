---
title: shields.io - 生成简洁、一致、清晰的徽章
date: 2024-02-28T13:51:42+08:00
lastmod: 2024-02-28T13:51:42+08:00
tags:
  - github
  - markdown
categories:
  - 服务
---

## 简介

![](./readme-logo.svg)

![Website][website-img]
![Build][build-img]
![License][lic-img]

|         |                                     |
| ------- | ----------------------------------- |
| 网站    | <https://shields.io>                |
| 仓库    | <https://github.com/badges/shields> |
| 文档    | <https://shields.io/docs>           |
| License | [CC0 1.0 Universal][lic-url]        |

[build-img]: https://img.shields.io/circleci/project/github/badges/shields/master
[lic-img]: https://img.shields.io/github/license/simple-icons/simple-icons
[lic-url]: https://github.com/badges/shields/blob/master/LICENSE
[website-img]: https://img.shields.io/website?url=https%3A%2F%2Fshields.io

[Shields.io](https://shields.io) 是一项简洁、一致、易读的徽章服务，可以轻松地将徽章包含在 GitHub 的阅读主题或任何其他网页中。

该服务支持数十种持续集成服务、软件包注册中心、发行版、应用商店、社交网络、代码覆盖服务和代码分析服务。世界上一些最受欢迎的开源项目都在使用它。

---

## 使用

### 静态徽章

#### 格式

- Label-Message 格式

  `https://img.shields.io/badge/{标签}-{信息}-{颜色}`

- 只有 Message 的格式

  `https://img.shields.io/badge/{信息}-{颜色}`

#### 颜色

> 颜色支持 Hex、rgb、rgba、hsl、css 名称

#### 转义字符

> | URL           | badge 输出 |
> | ------------- | ---------- |
> | 单下划线 `_`  | 空格 ` `   |
> | `%20`         | 空格 ` `   |
> | 双下划线 `__` | 下划线 `_` |
> | 双短横 `--`   | 短横 `-`   |

#### 其他参数

- style `string`
  - 徽章样式
  - 可选参数，默认为 `flat`
  - 可用的值： `flat` `flat-square` `plastic` `for-the-badge` `social`
- logo `string`
  - 可命名的 logo
  - 可选参数
  - 可用的值： `bitcoin` `dependabot` `gitlab` `npm` 等等，具体可参照 <https://simpleicons.org> 中的 logo 名称
- logoColor `string`
  - logo 颜色
  - 可选参数
  - 支持 Hex、rgb、rgba、hsl、css 名称

其他参数可查阅：<https://shields.io/badges/static-badge>

#### 示例

|            |                                                                                         |
| ---------- | --------------------------------------------------------------------------------------- |
| ![][img1]  | `https://img.shields.io/badge/platform-Windows-0078D4`                                  |
| ![][img2]  | `https://img.shields.io/badge/platform-Windows-black`                                   |
| ![][img5]  | `https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&logoColor=yellow`    |
| ![][img3]  | `https://img.shields.io/badge/Windows-8A2BE2`                                           |
| ![][img4]  | `https://img.shields.io/badge/Windows-0078D4?logo=windows&logoColor=DD0700`             |
| ![][img6]  | `https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows`                     |
| ![][img7]  | `https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=flat-square`   |
| ![][img8]  | `https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=plastic`       |
| ![][img9]  | `https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=for-the-badge` |
| ![][img10] | `https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=social`        |

[img1]: https://img.shields.io/badge/platform-Windows-0078D4
[img2]: https://img.shields.io/badge/platform-Windows-black
[img3]: https://img.shields.io/badge/Windows-8A2BE2
[img4]: https://img.shields.io/badge/Windows-0078D4?logo=windows&logoColor=DD0700
[img5]: https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&logoColor=yellow
[img6]: https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows
[img7]: https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=flat-square
[img8]: https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=plastic
[img9]: https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=for-the-badge
[img10]: https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows&style=social

### 动态徽章

可集成其他服务，显示服务状态

#### 示例

|                       |                  |
| --------------------- | ---------------- |
| ![][codecoverage-img] | 代码质量分析     |
| ![][buildstatus-img]  | 构建状态         |
| ![][release-img]      | Release Version  |
| ![][downloads-img]    | Python 包 下载数 |

[codecoverage-img]: https://img.shields.io/coveralls/github/badges/shields
[buildstatus-img]: https://img.shields.io/circleci/project/github/badges/shields/master
[release-img]: https://img.shields.io/badge/version-1.2.3-blue
[downloads-img]: https://img.shields.io/badge/downloads-13k%2Fmonth-brightgreen

更多服务集成：<https://shields.io/badges>
