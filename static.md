#static
1.static修饰局部变量的时候，局部变量就算出了作用域，也不会销毁，本质上，static修饰局部变量的时候，改变了变量的存储位置
```c
void test(){
    int a=1;
    a++;
    printf("%d",a);
}
int main(){
    int i0;
    while(i<10){
        test();
        i++;
    }
    exit(0);
}//以上代码会输出十个2；
void test(){
    int static a=1;
    //只要这样修改 就会输出2到11
}
```
*局部变量是放在栈的，而静态变量则放在静态区*
加上了static之后 变量的生命周期就会和程序一样长
2.static修饰全局变量
```c
static int c_bD=1106;
int main(){
printf("%d",c_bD)
}
//static修饰全局变量的时候 这个全局变量的外部链接属性就变成了内存链接属性
// 其他的源文件(.c)就不能再使用这个全局变量了
```
3.static修饰函数
```c
int getSum(int x,int y){
    return x+y;
}
int main(){
    int a=10;
    int b=20;
    int z=getSum(a,b);
    printf("%d\n",z);
    exit(0);
}

```
别的文件里的函数和变量要使用的时候使用
```c
extern
```
这个关键字 如果要使用的外部变量和函数被static修饰之后 它们就不再具有外部链接属性 无法使用 因为被修饰之后 它们变成了内部链接属性 其他的源文件无法使用

#register 寄存器
*一个电脑上的存储设备有哪些？*
除了内存和硬盘
还有**高速缓存（cache）**和**寄存器（集成在cpu）**
按照速度来排序 为 寄存器 高速缓存 内存 硬盘 
越往上空间越小 速度越快 造价越高
```c
int main(){
    //寄存器变量
    register int num=3;//建议把e放到寄存器当中 读取更快
    int *p=&num;
    printf("%d\n",*p);
    exit(0);
}
```
```