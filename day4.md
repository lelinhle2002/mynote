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
2.	Cho mảng một chiều n phần tử nguyên, nhập và in ra màn hình xem mảng có bao nhiêu phần tử âm và bao nhiêu phần tử dương.
```cpp
int main()
{
    int n;
    cout<<"nhap n"<<endl;
    cin>>n;
    int a[n];
    for(int i=0;i<n;i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
    int phantuam=0;
    int phantuduong=0;
    for(int i=0;i<n;i++)
    {
        if(a[i]>0)
        {
            phantuduong=phantuduong+1;
        }
        else phantuam=phantuam+1;
    }
    cout<<"phan tu am = "<<phantuam;
    cout<<"phan tu duong = "<<phantuduong;

}
```
