12.	Viết chương trình nhập vào 3 số a,b,c (1<= c <=3) nếu nhập số âm thì yêu cầu nhập lại. Nếu c=1 in ra tổng a+b, c=2 in ra hiệu a-b, Còn nếu c=3 thì in ra màn hình: " Tớ thích cậu rồi đấy!".
```cpp
int main()
{
    int a,b,c;
    do {
        cout<<"nhap a,b,c"<<endl;
        cin>>a>>b>>c;
    }while (a<0||b<0||c<0);

    if(c==1)
    {
        cout<<"tong a+b la"<<a+b;
    }
    else if(c==2)
    {
        cout<<"hieu a-b la"<<a-b;
    }
    else if(c==3)
    {
        cout<<"to thich cau roi day"<<endl;
    }
    return 0;
}

```
11.	Viết chương trình nhập vào n và in ra màn hình n!
```cpp
int main()
{
 int n;
 int giaithuan=1;
     cout << "nhap n"<<endl;
     cin>>n;
    for(int i=1;i<=n;i++)
    {
        giaithuan=giaithuan*i;
    }
    cout<<"giai thua n="<<giaithuan<<endl;

}
```
13.In ra bảng cửu chương 
```cpp
int main()
{

    for(int so=1; so<=9; so++)
    { cout<<"bang cuu chuong"<<so<<endl<<endl;

        for(int i=0; i<=10; i++)
        {

            cout<<so<<"x"<<i<<"="<<so*i<<endl;
        }
    }
}
```
6.	Viết chương trình nhập vào 1 số n và in ra màn hình các số nguyên tố trong khoảng từ 1 tới 2n.
```cpp
int main()
{
    int n;
    cin>>n;
    for(int j = 1 ; j <2*n; j++)
    {


        int demuoc=0;
        for(int i=1;i<=j;i++)
        {
            if(j%i==0)
            {
                demuoc=demuoc+1;
            }
        }
        if (demuoc==2)
        {
            cout<<j<<endl;
        }
    }
}
```
