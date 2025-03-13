# 使用 Devcontainer 开发

该项目包含一个 Devcontainer 配置，可以让你在一个预配置完整的开发环境中打开本项目。
当容器启动时，将同时初始化前端和后端环境。

## GitHub Codespaces

[![在 GitHub Codespaces 中打开](https://github.com/codespaces/badge.svg)](https://codespaces.new/langgenius/dify)

点击上面的按钮，即可在 GitHub Codespaces 中打开本项目。  
有关更多信息，请参见 [GitHub 文档](https://docs.github.com/en/free-pro-team@latest/github/developing-online-with-codespaces/creating-a-codespace#creating-a-codespace)。

## VS Code Dev Containers

[![在 Dev Containers 中打开](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/langgenius/dify)

如果你已经安装 VS Code，点击上面的按钮即可在 VS Code Dev Containers 中打开项目。  
更多信息请参考 [Dev Containers 文档](https://code.visualstudio.com/docs/devcontainers/containers)。

## Devcontainer 的优点

- 统一开发环境：确保所有开发者在相同的环境下开发，避免“在我的机器上运行正常”的问题。
- 快速启动：新开发者无需花大量时间配置环境，几步即可开始开发。
- 环境隔离：将项目与主机系统隔离，减少操作系统更新或其它软件安装对开发环境的影响。

## Devcontainer 的缺点

- 学习曲线：对于不熟悉 Docker 和 VS Code 的开发者来说，使用 Devcontainers 可能略显复杂。
- 性能影响：尽管通常影响不大，但容器内运行的程序可能比直接在主机上运行稍慢。

## 故障排查

如果你在 Codespaces 中打开项目时遇到如下错误：
![描述性文字](troubleshooting.png)

一种简单的解决方法是将 `/signin` 端点改为其他端点，使用 GitHub 账号登录后关闭标签页，再将其改回 `/signin`。  
这是因为 Codespaces 不允许直接使用 `signin` 端点，详细信息请参见 [这里](https://github.com/orgs/community/discussions/5204)
