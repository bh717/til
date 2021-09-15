# Node.js 包管理器的管理器 Corepack 的介绍和使用

### 什么是 `Corepack` ？

用于关联 `Node.js` 项目和包管理器的 `Node.js` 内置工具包。目前内置了 `yarn` 和 `pnpm` 包管理器。

### 如何使用 `Corepack` ？

- `corepack enable` 下载并激活所有的包管理工具（目前包括：`yarn`/`pnpm`）
- `corepack enable yarn` 下载并激活 `yarn`
- `corepack disable` 禁用所有的包管理工具（目前包括：`yarn`/`pnpm`）
- `corepack disable` 禁用 `yarn`
- `corepack prepare` 根据 `packageManager` 配置字段缓存对应的包管理器
- `corepack prepare package_manager@version --activate` 缓存并激活指定的包管理器和版本
- `corepack npm|pnpm|yarn package_manager_arguments` 非全局安装的情况下执行对应的命令

> `which corepack` 查看 `corepack` 的执行文件目录
