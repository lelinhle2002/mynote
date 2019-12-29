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
