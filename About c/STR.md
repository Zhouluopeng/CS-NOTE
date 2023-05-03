#字符串
```c
"hello world"
```
这种由双引号包起来的一串字符叫做字符串（String）
字符串结尾时使用\0
```c
int main(){
    #include <string.h>
    // char 字符类型 'a' 'b'
    //"sdjkfh" 字符串
    //C语言中没有字符串类型
    //描述字符串的时候用双引号
    "djshalks";
    char arr [10]="abcdefg";
    char arr1 []="askjhdgawdhj";
    //打印字符串是用转义字符%s
    printf("%s\n",arr1);
    //以上两种写法都可以
    char arr3[]={'1','2','a','b','e','\0'};//这种写法一定要
    //有\0 否则打印出来会带出来后面内存区域的东西
    int len=strlen(arr1);//求字符串长度的一个函数 ，string length
    //使用时要引入头文件 <string.h>
    printf("%d\n",strlen(arr1));
    return 0;
}
```