# c-programming-language
c语言程序设计

lab4 :
ex1 : 书上67页 练习4-3
ex2 : 书上67页 练习4-4


lab3 : 
ex1 : 书上 60 页，练习 4 1. 在 main 函数中调用该函数，处理用户输入的 2 个字符数组 s 和 t ，2个字符数组之间用空格区分，程序运行完打印 t 在 s 中最右边出现的位置，如果 s 中不包含 t, 打印 -1. 用户的输入最多不会超过200个字符，第一个字符串和第二个字符串中间用空格间隔，输入结束按回车。

ex2 : lab2 ex3

lab2 :
Ex1 : 编写一个程序找出你机器的 unsigned int 这种数据类型能存储的最大整数和这个最大整数的bit位数，并把它们打印出来。bit位数就是整数二进制表达的位数。

Ex2 : 把lab 1的第二题用getchar来实现，不能用scanf. 并且不能用取余%这个运算符，也就是不能用取余来算1的个数。要用比特位运算符来计算1的个数并输出。


Ex3 ：编写一个程序，提示用户输入一个16进制的非负整数，然后把用户输入的16进制数转换成10进制数打印出来。
用户输入的数据要以“0x”开头，x可以大写也可以小写。“0” – “9”，“a”-“f”, “A” – F” 是合法的数字字母字符组合，如果出现其他字符，均为非法的输入，需要告诉用户输入了不合法的字符，然后程序退出。
如果用户输入的16位表示的正整数超过了unsigned int能够存放的最大值，需要打印数据太大，告诉用户输入的数字太大，需要换一个小的数字，并把系统最大能够接受的整数(这个数是题目1的练习做出来的。)打印出来告诉用户。
这道题不能用scanf来做，因为要自己处理用户输入出错的情况。这道题用到的数据类型只能是unsigned int 或者int 和 char,不能使用long, long long等类型。不能用神奇数字作为数组的大小。所谓神奇数字，就是一个非计算出来的数字。



lab 1 :
题目 1 ：
已知摄氏温度为 0 5 10 15 20 25 30 一直到 100 度，
步长为 5 ，要求打印的结果要有表的抬头（包括了摄氏温度和华氏温度的名称），也就是第一行是摄氏温度对华氏温度表的英文。每一行第一个显示摄氏温度，再空2格显示华氏温度，清晰可辨认。参考书上第6页上的打印格式。

题目 2 ：编写一个程序，统计用户输入的一个非负整数的二进制表达中二进制位是 1 的位的个数，并且打印出这个个数。把源代码保存成 bc.c
非负整数不会超过 5 位数字，即可以假设最大的输入数字为 99999
例如，程序运行后，提示用户输入一个非负整数，用户在键盘上输入 36 ，按下回车键，程序应该打印数字 2 出来并且结束运行。这里 36 = 10 0100

题目二的解题思路 ：
题目二主要分为2个部分来解决
第一个部分，处理用户的输入：
用到getchar() 来获取用户的输入字符。 用户输入的字符是‘0’ – ‘9’之间的，要把用户输入的字符转换成数字。 转换成数字后，还要把每一个数字结合起来成为一个正整数的输入数值。10进制数每一位数字有的情况下，怎么结合？ 举个例子 36， 有3 和6两个数字，3 * （10的一次方） +  6 * （10的0次方）
数字字符转换成整数数值的方法，可以看一下对应的ASCII 码，C语言是用ASCII来编码的，https://www.ascii-code.com/ 看一下字符 ‘9’ 对应的整数数值和 字符‘0’对应的整数数值差了多少？
第一个部分处理用户输入需要把第一章的书本内容看一遍，上面的例子自己试一下编译运行。

第二个部分 ： 数二进制表达中数字1的个数，这里面可以用到 >> 1 ,这个操作可以把一个数值right shift 1位的意思，也就是会把一个数值缩小一半，一直对这个数right shift最后会把这个数值变成 0. 要注意编程的时候，要改变一个变量的值是通过赋值来完成，如果只进行 （a>>1 ）,这个操作不能改变a的值，只是会得出一个以a的值进行右移操作后的数值而已。 怎么看某一位是不是1 ，要用到其他的位运算符，具体要看书本第二章的内容。

