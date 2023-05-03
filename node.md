#c语言中的常量；
```c
int main(){
//1.字面常量
    30;
    3.14;
    "w";
    "abc";
//2.const修饰的常变量
const int a=10;//这个变量无法修改
//const所修饰的a，本质上是变量，但是不能直接修改，有常量的属性
}
//3.define所定义的标识符常量
#define MAX 100
#define STR "abcdefg"
int main(){
    printf("%d\n",MAX);
    int a=MAX;
    printf("%d\n",a);
    printf("%s\n",STR);
    return 0;
}
//4.枚举常量
enum Color{
    RED,
    GREEN,
    BLUE
};
//性别
enum Sex{
    MALE,
    FEMALE,
    SECRET
};
int main(){
    //三原色
    //RED GREEN BLUE
    enum Color c=RED;
    return 0;
}