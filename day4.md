1. Viết hàm kiểm tra xem 1 số có phải là số nguyên tố hay không. Dùng hàm vừa viết in ra các số nguyên tố từ 1->100.
```cpp
int hamkiemtra(int i)
{   int demuoc=0;
    for(int j=1; j<=i; j++)
    {
        if(i%j==0)
        {
            demuoc=demuoc+1;
        }
    }
    if(demuoc==2)
    {
        return 1;
    }
    else{return 0;}
}
int main()
{
    for(int i=1;i<=100;i++)
    {
        if(hamkiemtra(i)==1)

    cout << i << endl;}
    return 0;
}
```
