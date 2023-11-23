
# 如何使用 Hugo 在 Windows 上制作网站

## 准备工作
1. **安装 V2ray**：
   - 首先，安装 V2ray 以设置 VPN。这是重要的初始步骤，因为后续所有操作都需要通过 VPN 进行。
   - V2ray 软件的 Git 项目地址：[V2rayN GitHub](https://github.com/2dust/v2rayN)

2. **安装必要的软件**：
   - **安装 Chocolatey**：Windows 的包管理器，用于安装其他软件。[Chocolatey 安装页面](https://chocolatey.org/install)
   - **安装 Git**：版本控制系统，必需用于管理 Hugo 网站的代码。[Git 下载页面](https://git-scm.com/download/win)
   - **安装 Go**：Go 语言环境，用于运行一些 Hugo 的扩展功能。[Go 安装指南](https://go.dev/doc/install)
   - **安装 Visual Studio Code (VSCode)**：代码编辑器，用于编写和编辑网站代码。[VSCode 下载页面](https://code.visualstudio.com/)

3. **安装 Hugo 和 Dart-Sass**：
   - 在 Windows 命令行中输入以下命令来安装 Hugo Extended 版本和 Dart-Sass：
     ```
     choco install hugo-extended
     choco install sass
     ```

## 开始制作网站
1. **设置 Git Bash 的代理**：
   - 在开始使用 Git Bash 之前，您需要配置代理设置：
     ```
     git config --global http.proxy '127.0.0.1:10809'
     git config --global https.proxy '127.0.0.1:10809'
     ```

2. **克隆项目仓库**：
   - 在工作目录下打开 Git Bash。
   - 运行命令：
     ```
     git clone https://github.com/medic666/gzpharmacos.git
     ```

3. **启动 Hugo**：
   - 打开 VSCode，在相同工作目录下。
   - 使用 `Ctrl+`~` 快捷键打开命令行。
   - 启动 Hugo 服务器：
     ```
     hugo server
     ```

4. **预览和编辑网站**：
   - 使用浏览器打开 `localhost:1313` 来预览网站。
   - 在 VSCode 中编辑网站代码，Hugo 服务器将提供实时预览。

5. **上传更改到远程仓库**：
   - 在完成网站编辑后，您可以使用 Git Bash 将更改上传到远程仓库：
     ```
     git push
     ```