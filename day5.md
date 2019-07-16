5.	Cho mảng 1 chiều gồm n phần tử nguyên, sắp xếp lại mảng tăng dần. Rồi in ra màn hình.
```cpp
void nhapmang(int a[], int n)
{
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
}
void xuatmang(int a[], int n)
{
   for(int i=0;i<n;i++)
   {
       cout<<" "<<a[i]<<" ";
   }
}
void sapxep(int a[], int n)
{
    int k=0;
    for(int i=0; i<n-1;i++)
    {
        for(int j=i+1;j<n;j++)
        {
            if(a[i]<a[j])
        {
            k=a[i];
            a[i]=a[j];
            a[j]=k;
        }
        }
    }
}
int main()
{    int a[100];
     int n;
     int x;
     cout<<"nhap n"<<endl;
     cin>>n;
     nhapmang(a,n);
     cout<<"xuat mang vua nhap "<<endl;
     xuatmang(a,n);
     sapxep(a,n);
     cout<<"sau khi sap xep "<<endl;
     xuatmang(a,n);

}
```
