## bài 4
4.	Viết chương trình nhập vào số n và in ra màn hình dãy như sau: 1 3 5......n .... 6 4 2 ( nghĩa là dãy số có các số nguyên dương lẻ nhỏ hơn n nằm bên tay trái còn các số chẵn sẽ nằm bên tay phải.) 

```cpp

#include<iostream>


using namespace std;
int main()
{
    int n;
    cout<<"nhap n=";
    cin>>n;

    for(int i = 1;i <= n; i++) {
        if(i%2!=0)
            cout<<i<<" ";
    }

    for(int i = n; i >= 0; i--)
    {
        if(i%2==0) {
            cout<<i<<" ";
        }
    }
}
```
