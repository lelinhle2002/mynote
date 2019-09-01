1. tìm kiếm phần tử x trong mảng
```cpp
void nhapmang(int a[], int n)
{
    for(int i=0; i<n; i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
}
void xuatmang(int a[], int n)
{
    for(int i=0; i<n; i++)
    {
        cout<<a[i]<<" ";
    }
}
int timkiem(int a[], int n, int x )
{
    for(int i=0;i<n;i++)
    {
        if(a[i]==x)
        {
            return 1;
        }
    }
    return 0;
}
int main()
{
    int a[100];
    int n,x;
    cout<<"nhap n";
    cin>>n;
    nhapmang(a,n);
    xuatmang(a,n);
    cout<<" nhap x ";
    cin>>x;
    if (timkiem(a,n,x)==1)
    {
        cout<<" x co trong mang ";
    }
    else cout<"x ko co trong mang ";
}
```
