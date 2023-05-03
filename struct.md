#结构体
```c
struct student{
    //成员
    char name[20];
    int age;
    char sex[10];
    char phoneNumber[12];
};//这相当于是个图纸

void print(struct student* stu){
    printf("%s %d %s %s",ps->name,ps->age,ps->sex,ps->phoneNumber);
}

int main(){
    struct student mike={"mike",20,"man","123321123321"};
    //结构体对象 成员名
    printf("%s %d %s %s",s.name,s.age,s.sex,s.phoneNumber);
    print(&mike);
    exit(0);
}