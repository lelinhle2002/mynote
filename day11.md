7.	Cho mảng 1 chiều gồm n phần tử nguyên, nhập vào một phần tử x, xóa phần tử thứ x trong mảng, sau đó thay thế nhưng số 8 trong mảng bằng x, tiếp theo chèn thêm số 9 vào vị trí x+2. Mỗi thao tác thực hiên xong in kết quả ra màn hình.
```cpp
using namespace std;
void nhapmang(int a[], int n)
{
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
}

void xoaphantu(int a[], int n, int x)
{
    for(int i=x; i<n; i++)
    {
        a[i]=a[i+1];
    }
    n--;
}
void thaythe(int a[], int n, int x)
{
    for(int i=0; i<n; i++)
    {
        if(a[i]==8)
        {
            a[i]=x;
        }
    }
}
void chen(int a[], int n, int x)
{
    for(int i=n; i>=x+2; i-- )
    {
        a[i]=a[i-1];
    }
    a[x+2]=9;
    n++;
}
void xuatmang(int a[], int n)
{
    for(int i=0; i<n; i++)
    {
        cout<<a[i]<<" ";
    }
}

int main()
{
    int a[100];
    int x,n;
    cout<<"nhap n";
    cin>>n;
    cout<<"nhap mang A";
    nhapmang(a,n);
    cout<<"nhap x";
    cin>>x;
    cout<<"\n mang sau khi xoa\n";
    xoaphantu(a,n,x);
    xuatmang(a,n);
    cout<<"\n mang sau khi chen\n";
    chen(a,n,x);
    xuatmang(a,n);
    cout<<"\n mang sau khi thay the \n";
    thaythe(a,n,x);
    xuatmang(a,n);
}
```
