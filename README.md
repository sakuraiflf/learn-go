# Golang问题记录
记录遇到的Golang问题

1、go mod 导入自定义包，路径要从最外层包开始写


wsl安装记录
确保系统为
开linux子系统
安装wsl
开虚拟机
安装wsl2
安装内核更新
设置默认为2
安装分发版
换源
设置root密码
安装go
设置gopath

安装桌面版docker
卸载版本后wsl.exe闪退，wsl -l 查看默认的变了，wsl --setdefault Ubuntu-18.04修改下

sudo 找不到go命令 sudo visudo 在source_path加上GOPATH,不要直接修改sudoers的权限，sudo会直接废掉，wsl下我最后只能重装解决
go env -w GO111MODULE=on
 go env -w GOPROXY=https://goproxy.cn,direct

nano 编辑器ctrl+某个键进行操作

安装docker

安装beego

安装protobuf
protoc 文件放到bin


安装micro

导入、编译包记得使用模块名，要引用到具体的包别名才会生效，
linux 在/etc/bash.bashrc 下alias lll='klsdjfoasf fasds'的形式添加快捷命令 

VS pch.h/.cpp 预编译头，可以理解为，把一个基本不改变的头文件，编译成类似库的一个中间件，然后其他编译单元编译时就不需要去解析编译那个头文件了，而是直接把这个中间件加进去，从而显著提高编译速度。但C/CPP的编译单元是以源文件为单位的，单独的头文件并不能直接编译，而是作为一个字符串，直接替换掉源文件的include，再去编译展开后的源文件。（可以类比为宏的模式，宏在编译时也是不存在的，而是直接展开掉）所以MSVC编译器在实现预编译功能时，最简单的方法就给预编译头配对一个源文件，把它作为编译单元编译成中间件，这样可以复用绝大部分已有的设计。



