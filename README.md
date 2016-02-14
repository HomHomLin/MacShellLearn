# MacShellLearn

MacShell的学习笔记

1.Mac Shell的打印怎么写？
答：Mac Shell中 echo 代表打印。
echo hello world.则会在Command中打印出hello world.

2.如何打印环境变量的内容？
答：我们知道在Mac下的环境变量全部放置在/etc/profile/这个文件中。打印则是echo，那么打印环境变量内容则是：
echo $PATH
这样会在Command中打印出所有环境变量，但也许我们只需要其中一个环境变量，比如JAVA_HOME，那么我们只需要：
echo $JAVA_HOME
即可，$符号后面跟着环境变量的具体名字。

3.如何设置变量？
答：在mac shell中，我们可以直接对一个变量进行赋值，以下都是可以的：
AppName=Test
FOLDER=./${JAVA_HOME}_Release_201 或者 FOLDER=./$JAVA_HOME_Release_201

4.如何模拟Windows-bat的pause命令？
答：windows-bat的pause命令用于暂停等待用户输入操作再执行下一步，我们可以在mac shell中使用：
read -p "enter to go on"
命令来模拟pause命令，read用于读取用户输入的内容。

5.如何读取用户输入的内容？
答：首先我们需要一个保存变量，比如content，然后使用read命令：
read content
然后输入输入的内容就会被保存在conten中。

6.我打印环境变量内容，可是却打印出了“”空内容是什么情况？
答：环境变量有两个地方，一个是系统环境变量，位于/etc/profile中，另一个是在～下的.bash_profile文件，比如我们要打印JAVA_HOME，如果没有打印出内容，需要我们去检查这两个地方是否有JAVA_HOME环境变量。
在修改完任意一个环境变量后，都需要我们再输入source .bash_profile来更新环境变量。

7.声明变量后，我需要如何使用TA？
答：比如我们声明了环境变量N，并赋值100。那么脚本如下：
N＝100
我们如何打印？
echo $N
在使用变量前加上$符号，那么我们还可以怎么做？
echo ${N}

