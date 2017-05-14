# 输入与输出

## printf

`printf`函数用于格式化输出。

```c
printf("Height: %d\n", height);
```

`printf`的第一个参数是格式字符串，里面使用百分号`%`表示占位符，上面代码的`%d`就是占位符。`printf`的第二个参数代表填入第一个占位符的值，第三个参数代表第二个占位符，以此类推。

占位符的第一个符号总是百分号，第二个符号是一个字母，表示填入此处的值的类型。

- `%d`：整数`int`
- `%f`：浮点数`float`
- `%e`：科学计数法，使用指数表示一个值

百分号与类型字母之间，还可以插入一个整数，表示最小字段宽度。比如，`%4d`表示显示一个最低4位的整数，不足4位的整数头部将补上空格，4位及4位以上的整数不受影响。如果加上负号`%-4d`，不足4位的空格将加在整数尾部。

对于浮点数，还可以指定小数点之后要显示多少位。

```c
printf("Profit: %.2f\n", profit);
```

## scanf

`scanf`函数用于读取用户的键盘输入。

```c
scanf("%d", &i)
```

上面的代码表示，用户从键盘输入的是整数，将放入变量`i`。

`scanf`可以读取多个变量。

```c
scanf("%d%d%f%f", &i, &j, &x, &y);
```

`scanf`会忽略空白字符（包括空格符、水平制表符、垂直制表符、换页符和换行符），直到发现输入的字符匹配格式符为止。