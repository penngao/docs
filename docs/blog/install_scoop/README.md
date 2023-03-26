# 如何安装 scoop

## 环境需求

* Windows 7 SP1+ / Windows Server 2008+
* PowerShell 5 (或者更高版本，包括 PowerShell Core) 和 .NET Framework 4.5 (或更高版本)
* 为当前账户启用 PowerShell，例如 `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

## 安装

在 PowerShell 中运行一下命令，将 scoop 安装到默认的位置（c:\Users\<user>\scoop）

```powershell
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')

# or shorter
iwr -useb get.scoop.sh | iex
```

安装过程中遇到

```powershell
使用“1”个参数调用“DownloadString”时发生异常:“未能解析此远程名称: 'raw.githubusercontent.com'”

```

问题是 Github 访问失败，解决方案参考：

[安装包管理工具 scoop](https://blog.csdn.net/Amir_wu/article/details/102679155)

[修改 Hosts 解决 Github 访问失败](https://zhuanlan.zhihu.com/p/107334179)

一旦安装成功，运行 `scoop help` 验证是否成功。

<div align=center>
    <img width="300" src="./blog/install_scoop/assets/scoop help.JPG">
</div>


用户安装的程序和 scoop 本身位于 `c:\Users\<user>\scoop` 。全局安装的程序（`--global`）位于 `c:\ProgramData\scoop`。可以通过环境变量更改这些设置。具体步骤如下：

###  将 Scoop 安装到自定义目录（命令行方式）

```powershell
$env:SCOOP='D:\Applications\Scoop'
[Environment]::SetEnvironmentVariable('SCOOP', $env:SCOOP, 'User')
```

### 将全局程序安装到自定义目录（命令行方式）

```powershell
$env:SCOOP_GLOBAL='F:\GlobalScoopApps'
[Environment]::SetEnvironmentVariable('SCOOP_GLOBAL', $env:SCOOP_GLOBAL, 'Machine')
```

## 参考

[scoop](https://github.com/lukesampson/scoop)