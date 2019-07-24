nhập mảng, tìm các số hoàn hảo trong mảng 
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
  for(int i=0; i<n ;i++)
  {
      cout<<" "<<a[i]<<" ";
  }
}
int kiemtraso(int x)
{   int tong=0;
    for(int i=1;i<x; i++)
    {
         if(x%i==0)
         {
            tong=tong+i;
         }
    }
    if(tong==x)
    {
    return 1;
    }
    else return 0;
}
void xuatsohoanhao(int a[],int n)
{
    for(int i=0; i<n; i++)
    {
        if (kiemtraso(a[i])==1)
        {
            cout<<" "<<a[i]<<" ";
        }
    }
}
int main()
{
   int a[100];
   int n;
   cout<<"nhap n"<<endl;
   cin>>n;
   nhapmang(a,n);
   xuatmang(a,n);
   cout<<"\n cac so hoan hao trong mang la \n";
   xuatsohoanhao(a,n);
}
```
1.	Viết chương trình nhập vào dãy n phần tử và in ra các phần tử theo thứ tự ngược lại quá trình nhập. Số nhập đầu tiên sẽ in ra sau cùng.
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
    for(int i=0;i<n; i++)
    {
       cout<<a[i]<<" ";
    }
}
void sapxep(int a[], int n)
{
    int k=0;
    for(int i=0; i<n-1; i++)
    {
        for(int j=i+1; j<n; j++)

            {
                k=a[i];
                a[i]=a[j];
                a[j]=k;
            }


    }
}
int main()
{
    int a[100];
    int n;
    cout << "nhap n" << endl;
    cin>>n;
    nhapmang(a,n);
    xuatmang(a,n);
    sapxep(a,n);
    cout<<"sau khi sap xep ";
    xuatmang(a,n);
    return 0;
}
```
6.	Cho mảng một chiều gồm n phần tử nguyên, sắp xếp lại mảng sao cho nhưng phần tử âm thì tăng dần còn các phần tử dương thì giảm dần. Ví dụ: -9 -4 -2  8 7 5 1. In kết quả ra màn hình.
```cpp
void nhapmang(int a[], int n)
{
    for(int i=0; i<n; i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
}
void xuatmang(int a[],int n)
{
    for(int i=0; i<n; i++)
    {
        cout<<a[i];
    }
}
void sapxep(int a[], int n )
{
    int k=0;
    for(int i=0; i<n-1; i++)
    {
        for(int j=i+1; j<n; i++)
        {
            if(a[i]<0&&a[j]<0)
            {
                if(a[i]>a[j])
            {
                k=a[i];
                a[i]=a[j];
                a[j]=k;
            }
            }
          else
                if(a[i]>a[j])
                {
                    k=a[i];
                    a[i]=a[j];
                    a[j]=k;
                }

        }
    }
}
int main()
{
    int a[100];
    int n;
    cout<<" nhap n ";
    cin>>n;
    nhapmang(a,n);
    sapxep(a,n);
    cout<<" day sau khi sap xep ";
    xuatmang(a,n);
}
```
