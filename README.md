# c-programming-language
c语言程序设计

lab 1 :
题目 1 ：
已知摄氏温度为 0 5 10 15 20 25 30 一直到 100 度，
步长为 5 ，要求打印的结果要有表的抬头（包括了摄氏温度和华氏温度的名称），也就是第一行是摄氏温度对华氏温度表的英文。每一行第一个显示摄氏温度，再空2格显示华氏温度，清晰可辨认。参考书上第6页上的打印格式。

题目 2 ：编写一个程序，统计用户输入的一个非负整数的二进制表达中二进制位是 1 的位的个数，并且打印出这个个数。把源代码保存成 bc.c
正整数不会超过 5 位数字，即可以假设最大的输入数字为 99999
例如，程序运行后，提示用户输入一个非负整数，用户在键盘上输入 36 ，按下回车键，程序应该打印数字 2 出来并且结束运行。这里 36 = 10 0100

题目二的解题思路 ：
题目二主要分为2个部分来解决
第一个部分，处理用户的输入：
用到getchar() 来获取用户的输入字符。 用户输入的字符是‘0’ – ‘9’之间的，要把用户输入的字符转换成数字。 转换成数字后，还要把每一个数字结合起来成为一个正整数的输入数值。10进制数每一位数字有的情况下，怎么结合？ 举个例子 36， 有3 和6两个数字，3 * （10的一次方） +  6 * （10的0次方）
数字字符转换成整数数值的方法，可以看一下对应的ASCII 码，C语言是用ASCII来编码的，https://www.ascii-code.com/ 看一下字符 ‘9’ 对应的整数数值和 字符‘0’对应的整数数值差了多少？
第一个部分处理用户输入需要把第一章的书本内容看一遍，上面的例子自己试一下编译运行。

第二个部分 ： 数二进制表达中数字1的个数，这里面可以用到 >> 1 ,这个操作可以把一个数值right shift 1位的意思，也就是会把一个数值缩小一半，一直对这个数right shift最后会把这个数值变成 0. 要注意编程的时候，要改变一个变量的值是通过赋值来完成，如果只进行 （a>>1 ）,这个操作不能改变a的值，只是会得出一个以a的值进行右移操作后的数值而已。 怎么看某一位是不是1 ，要用到其他的位运算符，具体要看书本第二章的内容。

