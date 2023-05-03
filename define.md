#define定义常量和宏
```c
//定义变量
#define NUM 100
int main(){
    printf("%d",NUM);
    int n=NUM;
    printf("%d\n",n);
    int arr[NUM]={0};
    exit(0);
}
//define定义宏
//宏是有参数的
#define ADD(x,y) (( x )+( y ))
int main(){
    int a=10;
    int b=20;
    int c=ADD(a,b);
    printf("%d",c);
}
```
