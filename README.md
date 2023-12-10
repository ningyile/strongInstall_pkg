# strongInstall包
## 1 关于strongInstall包
<p align="center">
  <img src="https://raw.githubusercontent.com/ningyile/BDMCC_APP/main/img/mac_logo.png" width="20%" height="20%" />
</p>

- `strong包`为重症大数据行者（Big Data Master of Critical Care，BDMCC）的配套R包，可以批量执行sql、一键table1、一键多重插补、一键倾向性评分匹配、一键多种模型建模、一键写入发表级的table以及图表对象管理等功能，极大提高数据处理效率。安装`strong包`之前需要安装`strongInstall包`。
- `strongInstall包`支持Windows、macOS、Linux三种操作系统，实现对`strong包`及其依赖包一键安装，以及`strong包`后续的一键升级。

## 2 安装strongInstall包
- [单击此处](https://github.com/ningyile/strongInstall_pkg/releases)下载strongInstall包，根据不同的平台下载不同的二进制安装包。
- `strong包`仅支持R V4.2以上版本。

### 2.1 Windows下strongInstall包的安装
- Windows系统下载`strongInstall_1.0.1.zip`。然后依次单击Rstudio中的【Packages】、【Install】，然后在弹出的对话框单击【Browse】中选择相应下载路径中的`strongInstall_1.0.1.zip`即可。
<p align="center">
  <img src="https://raw.githubusercontent.com/ningyile/strongInstall_pkg/main/img/win.png" width="70%" height="70%" />
</p>
### 2.2 macOS下strongInstall包的安装
- Intel芯片的macOS系统下载`strongInstall_intel_1.0.1.tgz`，M系列芯片的macOS系统下载`strongInstall_apple_1.0.1.tgz`。然后依次单击Rstudio中的【Packages】、【Install】，然后在弹出的对话框单击【Browse】中选择相应下载路径中的`tgz文件`即可。
<p align="center">
  <img src="https://raw.githubusercontent.com/ningyile/strongInstall_pkg/main/img/mac.png" width="70%" height="70%" />
</p>

### 2.3 Linux下strongInstall包的安装
- Linux系统下载`strongInstall_1.0.1_R_x86_64-pc-linux-gnu.tar.gz`。然后依次单击Rstudio中的【Packages】、【Install】，然后在弹出的对话框单击【Browse】中选择相应下载路径中的`gz文件`即可。
<p align="center">
  <img src="https://raw.githubusercontent.com/ningyile/strongInstall_pkg/main/img/linux.png" width="70%" height="70%" />
</p>

## 3 strong包安装说明
- `strongInstall包`安装成功后，即可依次安装所需的依赖包和`strong包`。

### 3.1 一键安装依赖包
打开Rstudio，在控制台运行以下代码：
```R
strongInstall::install_strong_dep()
```
<p align="center">
  <img src="https://raw.githubusercontent.com/ningyile/strongInstall_pkg/main/img/install_dep.png" width="70%" height="70%" />
</p>


直至出现"  **-- 依赖包全部安装完毕 --** " 字样即可进行下一步以安装`strong包`。



### 3.2 一键安装strong包

在依赖包安装完毕后，在控制台运行以下代码以获取授权码：

```R
strongInstall::install_strong_pkg()
```
<p align="center">
  <img src="https://raw.githubusercontent.com/ningyile/strongInstall_pkg/main/img/install_pkg.png" width="70%" height="70%" />
</p>


上述代码初次运行后会出现一串序列号，根据提示复制序列号，然后发送给管理员进行授权。授权后再次运行`strongInstall::install_strong_pkg()`直至出现" **strong包安装成功！**" 字样即表明`strong包`安装成功。



### 3.3 一键升级strong包

后续加载`strong包`时若提示版本过低，则可根据提示在控制台运行`strongInstall::install_strong_pkg()`以安装最新版的`strong包`。

## 4 更新日志
- **V1.0.1** 初次发布，含一键安装依赖包和strong包功能。
