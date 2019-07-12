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
8.	Số chính phương là số mà căn bậc hai của nó là 1 số nguyên dương. Viết chương trình nhập vào một số nguyên dương n và cho biết trong khoảng từ 1 tới 2n có bao nhiêu số chính phương. Hãy in ra dãy số chính phương đó.
```cpp
int main()
{   int n;
    cout<<"nhap n"<<endl;
    cin>>n;
    for(int i=1;i<=2*n;i++)
    {
        int a=sqrt(i);
        float b=sqrt(i);
        if(a==b)
        {
            cout<<i<<endl;
        }
    }
}
```
14.	Viết chương trình nhập vào 2 số nguyên dương a,b tìm và in ra màn hình ước chung của chúng.
```cpp
int main()
{
    int a, b;
    cin>>a>>b;

    if(a > b)
    {
        int c = a;
        a = b;
        b = c;

    }


    int i = 1;

    while(i<b)
    {

        if(a%i==0&&b%i==0)
        {
            cout<<i<<endl;
        }
        i++;
    }
}
```
2. nhập 1 dãy số n phần tử, in ra các số chẵn.
```cpp
int main()
{
   int n,i;
   cout<<"nhap n"<<endl;
   cin>>n;
   int a[n];
   for(int i=0;i<n;i++)
   {
       cout<<"a{"<<i<<"]=";
       cin>>a[i];
}

for(int i =0 ;i <n; i++)
{
    if(a[i]%2==0)
    {

        cout<<a[i]<<" ";

    }
}

}
```
