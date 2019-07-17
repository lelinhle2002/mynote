viết hàm vào một mảng, hàm xuất mảng đó ra màn hình và xuất các sô snguyene tố trong dãy ra màn hình.
```cpp
void nhapmang(int a[],int n)
{
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
}
void xuatmang(int a[],int n)
{
    for(int i=0;i<n;i++)
    {
        cout<<a[i] <<endl;
    }
}
int kiemtrasnt(int x)
{   int demuoc=0;
    for(int i=1;i<=x;i++)
    {
        if(x%i==0)
        {
            demuoc++;
        }
    }
    if (demuoc==2)
    {
        return 1;
    }
    return 0;
}
void xuatsnt(int a[], int n)
{
     for(int i=0;i<n;i++)
     {
         if (kiemtrasnt(a[i])==1)
         {
             cout<<" "<<a[i]<<" ";
         }
     }
}
int main()
{
    int n;
    int a[100];
    cout<<"nhap  n"<<endl;
    cin>>n;
    cout<<"nhap mang ";
    nhapmang(a,n);
    cout<<"xuat mang ";
    xuatmang(a,n);
    cout<<" ";
    xuatsnt(a,n);
}
```
