5.	Viết chương trình nhập vào số nguyên dương n và in ra màn hình tổng các số chẵn khoảng từ 1 tới n.
```cpp
int main()
{   int n;
    cout << "nhap n"<<endl;
    cin>>n;
    for(int i=0;i<=n;i+=2)
    {
        cout<<i<<endl;
    }
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
