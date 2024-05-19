# Rust

##  基础入门

### 原生类型



### 自定义类型



### 变量绑定



### 类型系统



### 类型转换



### 表达式



### 流程控制



### 函数



### 模块



### crate



### 属性



### 泛型



### 作用域规则



### 特质 trait



### 使用macro_rules创建宏



### 错误处理



### 标准库类型



### 标准库更多介绍



### 测试



### 不安全操作



### 兼容性



### 补充







# Manjaro

## 系统指令

### 包管理

#### pacman

`pacman` 是 Arch Linux 及其衍生发行版中用于包管理的命令行工具。它主要用于安装、更新、卸载软件包以及管理系统的软件仓库。以下是一些基本的 `pacman` 指令及其用途：

```
sudo pacman -Sy #安装并更新软件包的数据库
sudo pacman -Syu # 更新并升级系统
pacman -Ss <search_term> # 搜索软件包
pacman -Si <package_name> # 查看软件包信息
pacman -Q # 列出已安装的软件包
```

```
sudo pacman -Rn <package_name> # 卸载软件包，同时删除配置文件
```

- 源配置

```
sudo pacman-mirrors -i -c China -m rank

sudo pacman -Syyu # 更新软件库
```

- AUR助手paru安装

AUR是Arch Linux社区维护的一个存储库，包含了大量的非官方或者实验性的软件包。通过克隆这个Git仓库，你获得了构建`paru`所需的全部源代码和构建脚本

```
sudo pacman -S --needed base-devel
git clone https://aur.archlinux.org/paru.git
cd paru
makepkg -si
#这个命令在paru目录下启动编译和打包过程。makepkg是一个用于从源代码构建Arch Linux软件包的工具。-s选项会在构建前检查依赖关系，并使用pacman安装缺少的依赖（如果之前没有使用--needed base-devel安装的话，这里可能会安装额外的依赖）。-i选项则在构建完成后立即安装生成的.pkg.tar.zst软件包。此步骤实质上是编译paru的源代码，并将其作为系统上的一个可执行程序安装，使得你可以开始使用paru来更方便地从AUR安装软件
```

配置出错了，更换了ustc源

```
sudo pacman -S archlinuxcn-keyring

archlinuxcn-keyring 包含了Arch Linux CN（中国）仓库的GPG密钥，
当你尝试从Arch Linux CN仓库安装软件时，系统需要验证软件包的完整性和真实性，以确保它们没有被篡改。安装 archlinuxcn-keyring 就是为了将这些必需的GPG密钥添加到你的系统中，从而使得 pacman 能够验证来自该仓库的软件包签名。
```

## 系统配置（快捷键）

### zsh主题修改

使用powerlevel10k进行zsh的主题管理

```
https://zhuanlan.zhihu.com/p/351037220
```

```
. ~/.zshrc 执行配置
```

- 中文的系统名称，但是~底下是英文

```
https://www.jianshu.com/p/73299b8e3f58
```

