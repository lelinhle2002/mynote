5.	Viết chương trình nhập vào số nguyên dương n và in ra màn hình tổng các số chẵn khoảng từ 1 tới n.
```cpp
int main()
{
    int n;
    cout<<"nhap n"<<endl;
    cin>>n;
    int tong=0;
    for(int i=1;i<=n;i++)
    {
        if(i%2==0)
        {
            tong=tong+i;
        }
    }
    cout<<"tong cac so chan tu 1 den n"<<tong;
}

```
7.	Viết chương trình nhập vào 2 số a,b và in ra màn hình các số nguyên tố trong khoảng bị giới hạn bởi a và b (Mọi người lưu ý là a,b nhập ngẫu nhiên nhé!)
```cpp
int main()
{
    int a,b;
    cout<<"nhap a,b"<<endl;
    cin>>a>>b;
    for(int i=a; i<=b; i++)
    {   int demuoc=0;
        for(int j=1;j<=i;j++)
        {
            if(i%j==0)
            {
                demuoc++;
            }
        }
        if(demuoc==2)
        {
            cout<<i<<endl;
        }
    }
}
```
9.	Viết chương trình tìm ra số lũy thừa 2 đầu tiên lớn hơn 1000.
```cpp
int main()
{
    int i = 0;
    while(true){
        double a = pow(i, 2);
        if(a > 1000){
            cout<<"so dau tien luy thua 2 lon hon 1000 la = "<<i;
            break;
        }
        i++;
    }

}
```
