# 1.2 简介

本节简单预览一下语言功能，有个相对完整的印象更利于学习后续知识。

{% hint style="info" %}
可依照第 12 章安装配置编译环境。
{% endhint %}

本书相关内容和示例运行环境：
- Mac OS EI Caption 10.11.4
- Ubuntu Server 14.04 x86_64
- GNU gcc 5.3 / gdb 7.7
- Go 1.6 amd64

## 源文件

源码文件使用 UTF-8 编码，对 Unicode 支持良好。每个源文件都属于包的一部分，在文件头部用 package 声明所属包名称。

**test.go**
```go
package main

func main() {
    println("hello, world!")
}
```

以 `.go` 作为文件扩展名，语句结束分号会被默认省略，支持 C 样式注释。入口函数 main 没有参数，且必须放在 main 包中。
```go
package main

import (
    "fmt"
)

func main() {
    funt.Println("hello, world!")
}
```
{% hint style="info" %}
否则编译器会将其当作错误。
{% endhint %}

可直接运行，或编译为可执行文件。
```bash
go run main.go

# 输出
hello, world!
```
