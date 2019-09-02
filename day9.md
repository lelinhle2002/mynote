
```cpp
#include <iostream>
#include<math.h>

using namespace std;

struct diemtoado
{
    int x;
    int y;
};
void nhaptoado(diemtoado &d)
{
    cout<<"nhap x ";
    cin>>d.x;
    cout<<"nhap y ";
    cin>>d.y;
}
void xuattoado(diemtoado d)
{
    cout<<"("<<d.x<<","<<d.y<<")";
}
double khoangcach(diemtoado d1, diemtoado d2)
{
    double kc;
    kc= sqrt(double(d1.x-d2.x)*(d1.x-d2.x)+(d1.y-d2.y)*(d1.y-d2.y));
    return kc;
}
int main()
{
    diemtoado A,B;
    float khoangcach;
    cout<<"diem A:";
    nhaptoado(x);
    cout<<"diem B:";
    nhaptoado(y);
    cout<<"toa do A la:";
    xuattoado(x);
    cout<<"toa do B la:";
    xuattoado(y);
    cout << "khoang cach giua 2 diem A,B: " << khoangcach;
    return 0;
}
```
2. chữa
```cpp
#include <bits/stdtr1c++.h>

using namespace std;
typedef struct diemtoado
{
    double x;
    double y;
};
double khoangcach(diemtoado d1, diemtoado d2)
{
    double kc;
    kc= sqrt((d1.x-d2.x)*(d1.x-d2.x)+(d1.y-d2.y)*(d1.y-d2.y));
    return kc;
}
int main()
{
   diemtoado A,B;
   cout<<"nhap tao do diem A:"<<endl;
   cin>>A.x>>A.y;
   cout<<"nhap toa do diem B:"<<endl;
   cin>>B.x>>B.y;
   cout<<"khoang cach giua hai diem A va B la:"<<khoangcach(A,B);
   return 0;
}
```
