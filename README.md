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

