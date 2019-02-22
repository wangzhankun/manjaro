一切皆文件，一切皆命令。

# shell bash

* 解释器
  * 用户交互输入
  * 文本文件输入

一切皆命令：

* 直接在bash编写函数
* 将命令写在文件中
* 四种执行方式：
  * source {filename}
  * . {filename}
  * ./{filename}
  * bash {filename}

# 重定向与文件流

0：标准输入

1：标准输出

2：标准错误输出

重定向输出操作符：

* \> 覆盖
* \>> 追加

# read

从标准输入读东西，对换行符及其敏感

注意三个\<与两个的区别。两个的时候可以按照任意字符作为首尾。

\<<本身是重定向操作，read也可以换位cat等。

![](D:\aboutme\STUDY\manjaro\pictures\read_command.PNG)

# exec

```
exec: exec [-cl] [-a name] [command [arguments ...]] [redirection ...]
    Replace the shell with the given command.
    
    Execute COMMAND, replacing this shell with the specified program.
    ARGUMENTS become the arguments to COMMAND.  If COMMAND is not specified,
    any redirections take effect in the current shell.
    
    Options:
      -a name	pass NAME as the zeroth argument to COMMAND
      -c		execute COMMAND with an empty environment
      -l		place a dash in the zeroth argument to COMMAND
    
    If the command cannot be executed, a non-interactive shell exits, unless
    the shell option `execfail' is set.
    
    Exit Status:
    Returns success unless COMMAND is not found or a redirection error occurs.

```

简单例子实现(获得百度主页)

```
exec 8<> /dev/tcp/www.baidu.com/80
echo -e "GET / HTTP/1.0\n" 1>&8
cat 0<&8
```

# 变量

## 本地

* 当前shell拥有
* 生命周期随shell

## 局部

* 只能local用于函数



## 特殊

* $#: 位置参数个数
* $*: 参数列表，双引号引用为一个字符串
* $@: 参数列表，双引号引用为单独的字符串
* $$: 当前shell的pid：接收者
  * $BASHPID: 真实
  * 管道
  * ![](D:\aboutme\STUDY\manjaro\pictures\bashpid.PNG)
  * $$优先级比bash高，$BASHPID比bash优先级低
  * 在执行管道时，就是同时创建两个bash，但是左边bash的标准输出会作为右边bash的标准输入
  * 子进程的操作无法改变父进程
* $?: 上一个命令的退出状态
  * 0：成功
  * other：失败

