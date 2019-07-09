## In Ra các số chẵn trong khoảng từ 1 đến 100

```cpp
#include<iostream>
using namespace std;
int main()
{
    for(int i=0;i<=100;i++)
    {
        if(i%2==0)
        {
            cout<<i<<endl;
        }
    }
}
```

## In ra các số chăn chia hết cho 5 trong khoảng tưừ 100 -> 1000

```cpp
#include<iostream>
using namespace std;
int main()
{
    for(int i=100;i<=1000;i++)
    {
        if(i%2==0&&i%5==0)
        {
            cout<<i<<endl;
        }
    }
}
```
