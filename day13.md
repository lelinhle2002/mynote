```cpp
struct doanh_nghiep
{
    char madoanhnghiep[30];
    char giamdoc[30];
    float vondieule;
    int sonhanvien;
};
void nhapdoanhnghiep(doanh_nghiep &x)
{
    cout<<"\n\nnhap ma doanh nghiep: ";
    fflush(stdin);
    gets(x.madoanhnghiep);
    cout<<"nhap giam doc: ";
    fflush(stdin);
    gets(x.giamdoc);
    cout<<"nhap von dieu le: ";
    cin>>x.vondieule;
    cout<<"nhap so nhan vien: ";
    cin>>x.sonhanvien;
}
void xuatdoanhnghiep(doanh_nghiep x)
{
    cout<<"\n\nma doanh nghiep: "<<x.madoanhnghiep<<endl;
    cout<<"giam doc: "<<x.giamdoc<<endl;
    cout<<"von dieu le: "<<x.vondieule<<endl;
    cout<<"so nhan vien: "<<x.sonhanvien<<endl;
}
void nhapdanhsach(doanh_nghiep y[], int n)
{
    for(int i=0; i<n ;i++)
    {
        nhapdoanhnghiep(y[i]);
    }
}
void xuatdanhsach(doanh_nghiep y[], int n)
{
    for(int i=0; i<n ;i++)
    {
        xuatdoanhnghiep(y[i]);
    }
}
int main()
{
    doanh_nghiep dsy[100];
    int n;
    cout<<" nhap n ";
    cin>>n;
    nhapdanhsach(dsy,n);
    xuatdanhsach(dsy,n);

    return 0;
}
```
2
```cpp
using namespace std;
struct doanh_nghiep
{
    char madoanhnghiep[30];
    char giamdoc[30];
    float vondieule;
    int sonhanvien;
};
void nhapdoanhnghiep(doanh_nghiep &x)
{
    cout<<"\n\nnhap ma doanh nghiep: ";
    fflush(stdin);
    gets(x.madoanhnghiep);
    cout<<"nhap giam doc: ";
    fflush(stdin);
    gets(x.giamdoc);
    cout<<"nhap von dieu le: ";
    cin>>x.vondieule;
    cout<<"nhap so nhan vien: ";
    cin>>x.sonhanvien;
}
void xuatdoanhnghiep(doanh_nghiep x)
{
    cout<<"\n\nma doanh nghiep: "<<x.madoanhnghiep<<endl;
    cout<<"giam doc: "<<x.giamdoc<<endl;
    cout<<"von dieu le: "<<x.vondieule<<endl;
    cout<<"so nhan vien: "<<x.sonhanvien<<endl;
}
void nhapdanhsach(doanh_nghiep y[], int n)
{
    for(int i=0; i<n ;i++)
    {
        nhapdoanhnghiep(y[i]);
    }
}
void xuatdanhsach(doanh_nghiep y[], int n)
{
    for(int i=0; i<n ;i++)
    {
        xuatdoanhnghiep(y[i]);
    }
}
void sapxep(doanh_nghiep y[], int n)
{
    doanh_nghiep k;
    for(int i=0; i<n-1 ; i++)
    {
        for(int j=i+1; j<n ;j++)
        {
            if(y[i].vondieule>y[j].vondieule)
            {
                k =y[i];
                y[i]=y[j];
                y[j]= k;
            }
        }
    }
}
int main()
{
    doanh_nghiep dsy[100];
    int n;
    cout<<" nhap n ";
    cin>>n;
    nhapdanhsach(dsy,n);
    xuatdanhsach(dsy,n);
    cout<<"\n sau khi sap xep: \n";
    sapxep(dsy,n);
    xuatdanhsach(dsy,n);

    return 0;
}
```
3.
```cpp
struct doanh_nghiep
{
    char madoanhnghiep[30];
    char giamdoc[30];
    float vondieule;
    float sonhanvien;
};
void nhap1dn(doanh_nghiep &x)
{
    cout<<"\n\nnhap ma doanh  nghiep: ";
    fflush(stdin);
    gets(x.madoanhnghiep);
    cout<<"nhap ten giam doc: ";
    fflush(stdin);
    gets(x.giamdoc);
    cout<<"nhap so von dieu le: ";
    cin>>x.vondieule;
    cout<<"nhap so nhan vien: ";;
    cin>>x.sonhanvien;
}
void xuatdn(doanh_nghiep x)
{
    cout<<"\n\nma doanh nghiep : "<<x.madoanhnghiep<<endl;
    cout<<"giam doc : "<<x.giamdoc<<endl;
    cout<<"von dieu le : "<<x.vondieule<<endl;
    cout<<"so nhan vien : "<<x.sonhanvien<<endl;
}
void nhap1ds( doanh_nghiep ds[], int n)
{
    for(int i=0; i<n ; i++)
    {
        nhap1dn(ds[i]);
    }
}
void xuat1ds( doanh_nghiep ds[], int n)
{
    for(int i=0; i<n ; i++)
    {
        xuatdn(ds[i]);
    }
}
void sapxep(doanh_nghiep ds[], int n)
{
    doanh_nghiep k;
    for(int i=0; i<n-1; i++)
    {
        for(int j=i+1; j<n; j++)
        {
            if(ds[i].vondieule > ds[j].vondieule)
            {
                k=ds[i];
                ds[i]=ds[j];
                ds[j]=k;
            }
        }
    }
}
void nhapdn(doanh_nghiep x)
{
    cout<<"ma doanh nghiep: "<<x.madoanhnghiep<<endl;
    cout<<"so nhan vien: "<<x.sonhanvien<<endl;
}
void inradn(doanh_nghiep ds[], int n)
{
    for(int i=0; i<n ; i++)
    {
        if(ds[i].sonhanvien>300&&ds[i].madoanhnghiep[0]=='D'&&ds[i].madoanhnghiep[1]=='N')
        {
            nhapdn(ds[i]);
        }
    }
}
int main()
{
    doanh_nghiep dsy[100];
    int n;
    cout<<"nhap n ";
    cin>>n;
    nhap1ds(dsy, n);
    xuat1ds(dsy, n);
    sapxep(dsy, n);
    cout<<"\n\nsau khi sap xep: \n\n"<<endl;
    xuat1ds(dsy,n);
    cout<<"\n\nin ra so nhan vien > 300 va madoanhnghiep bat dau =DN "<<endl;
    inradn(dsy, n);
}
```
