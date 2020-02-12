1.if 1<=n<=9 then print the lowercase English word corresponding to the number (e.g., one for , two for , etc.); otherwise, print Greater than 9 instead.
```cpp
string a[]={"Greater than 9","one","two","three","four","five","six","seven","eight","nine"};
    int n;
    cin>>n;
    cout<<((n>9)?a[0]:a[n]);
    return 0;
```
