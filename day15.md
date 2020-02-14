1, You have to complete the function void update(int *a,int *b), which reads two integers as argument, and sets a with the sum of them, and  with the absolute difference of them.


```cpp
void update(int *a,int *b) {
    // Complete this function  
    *a += *b;
    *b= 2*(*b)-*a;
    *b= *b>0 ? *b : -1*(*b);
    
};

int main()
{
    int a, b;
    int *pa = &a, *pb = &b;
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
```
