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
2. viết phương trình nhập n tọa dộ (x,y). tìm 2 tọa độ có khaongr cách lớn nhất in ra màn hình.
```cpp
using namespace std;
int x[100];
int y[100];
double dodai(int i, int j)
{
    double kq=sqrt(pow(x[j]-x[i],2)+ pow(y[j]-y[i],2));
    return kq;
}


void nhap_n_diem(int n)
{
    for(int i =0; i<n; i++)
    {
        cout<<"nhap vao toa do (x, y)"<<endl;
        cin>>x[i];
        cin>>y[i];
    }
}
int main()
{

    int n = 0;
    cout<<"nhap vao n ="<<endl;
    cin>>n;

    nhap_n_diem(n);
    int imax = 0;
    int jmax = 0;
    double do_dai_max = 0;
    for(int i=0; i< n; i++)
    {
        for(int j = 0; j < n; j++)
        {
            double ketqua = dodai(i, j);
            if(ketqua > do_dai_max)
            {
                do_dai_max = ketqua;
                jmax = j;
                imax = i;
            }
        }
    }


    cout<<"imax="<<imax<<endl;
    cout<<"jmax="<<jmax<<endl;

    cout<<"Diem 1 la="<<endl;
    cout<<"("<<x[imax]<<", "<<y[imax]<<")"<<endl;
    cout<<"Diem 2 la="<<endl;
    cout<<"("<<x[jmax]<<", "<<y[jmax]<<")"<<endl;
}
```
3. Xây dựng chương trình: Nhập số tự nhiên n có 4 chữ số. Hãy tìm và in ra màn hình chữ số hàng nghìn, hàng trăm, hàng chục, hàng đơn vị của n. 
```cpp
int main()
{
    int n;
    cout<<"nhap so tu nhien n"<<endl;
    cin>>n;
    int a=n/1000;
    int b=n%1000/100;
    int c=n%1000%100/10;
    int d=n%10;
    cout<<"chu so hang nghin: "<<a<<endl;
    cout<<"chu so hang tram: "<<b<<endl;
    cout<<"chu so hang chuc: "<<c<<endl;
    cout<<"chu so hang don vi: "<<d<<endl;
}
```
