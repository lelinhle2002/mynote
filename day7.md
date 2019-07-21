chuỗi ký tự và một số hàm xử lý 
```cpp

int main()
{
    char chuoi1[20];
    char chuoi2[20];
    cout<<"nhap chuoi 1";
    gets(chuoi1);
    cout<<"nhap chuoi 2";
    fflush(stdin);
    gets(chuoi2);
    cout<<"chuoi 1 : "<<chuoi1<<endl;
    cout<<"chuoi 2 : "<<chuoi2<<endl;
    cout<<strcmp(chuoi1,chuoi2);
    return 0;
}
 ```
