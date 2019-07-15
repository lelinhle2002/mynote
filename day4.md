1. Viết hàm kiểm tra xem 1 số có phải là số nguyên tố hay không. Dùng hàm vừa viết in ra các số nguyên tố từ 1->100.
```cpp
int hamkiemtra(int i)
{   int demuoc=0;
    for(int j=1; j<=i; j++)
    {
        if(i%j==0)
        {
            demuoc=demuoc+1;
        }
    }
    if(demuoc==2)
    {
        return 1;
    }
    else{return 0;}
}
int main()
{
    for(int i=1;i<=100;i++)
    {
        if(hamkiemtra(i)==1)

    cout << i << endl;}
    return 0;
}
```
2.	Cho mảng một chiều n phần tử nguyên, nhập và in ra màn hình xem mảng có bao nhiêu phần tử âm và bao nhiêu phần tử dương.
```cpp
int main()
{
    int n;
    cout<<"nhap n"<<endl;
    cin>>n;
    int a[n];
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
    int phantuam=0;
    int phantuduong=0;
    for(int i=0;i<n;i++)
    {
        if(a[i]>0)
        {
            phantuduong=phantuduong+1;
        }
        else phantuam=phantuam+1;
    }
    cout<<"phan tu am = "<<phantuam;
    cout<<"phan tu duong = "<<phantuduong;

}
```
3.	Cho mảng 1 chiều n phần tử nguyên, nhập và in ra màn hình kiểm tra xem trong mảng có bao nhiêu phần tử là ước của n.
```cpp
int main()
{
    int n;
    cout<<"nhap n"<<endl;
    cin>>n;
    int a[n];
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
    int uoc=0;
    for(int i=0;i<=n;i++)
    {
        if(n%a[i]==0)
        {
            uoc=uoc+1;
        }
    }
        cout<<"uoc cua a = "<<uoc;

}
```
4.	Cho mảng 1 chiều gồm n phần tử nguyên, kiểm tra và in ra màn hình những phần tử là số nguyên tố hoặc là số chính phương.
```cpp
int main()
{
    int n;
    cout<<"nhap n"<<endl;
    cin>>n;
    int a[n];
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
    int demuoc=0;
    for(int i=1;i<n;i++)
    {
        if(a[i]%i==0)
        {
            demuoc=demuoc+1;
        }
    }
    int songuyento=0;
    if(demuoc==2)
    {
        songuyento=songuyento+1;
    }
    cout<<"so cac so nguyen to la "<<songuyento;
    int x,y;
    int sochinhphuong=0;
    for(int i=0;i<n;i++)
    {
        float x= sqrt(a[i]);
        int y=sqrt(a[i]);
        if (x==y)
        {
            sochinhphuong=sochinhphuong+1;
        }
    }
    cout<<"so chinh phuong la "<<sochinhphuong;

}
```
