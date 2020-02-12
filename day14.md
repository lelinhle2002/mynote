1.if 1<=n<=9 then print the lowercase English word corresponding to the number (e.g., one for , two for , etc.); otherwise, print Greater than 9 instead.
```cpp
string a[]={"Greater than 9","one","two","three","four","five","six","seven","eight","nine"};
    int n;
    cin>>n;
    cout<<((n>9)?a[0]:a[n]);
    return 0;
```
2.Input Format

You will be given two positive integers,a  and b (a<=b), separated by a newline.

Output Format

For each integer n in the interval [a,b] :

If 1<=n<=9 , then print the English representation of it in lowercase. That is "one" for , "two" for , and so on.
Else if  and it is an even number, then print "even".
Else if  and it is an odd number, then print "odd".

```cpp
int main() {
    int a,b;
    string c[]={"","one","two","three","four","five","six","seven","eight","nine"};
    cin>>a>>b;
    for(int i=a;i<=b;i++)
        cout<<((i<=9)?c[i]:((i%2==0)?"even":"odd"))<<endl;
}
```
3.
```cpp
int max_of_four(int a,int b,int c, int d){

if(a > b){
    if(a > c){
        if(a>d)return a;
        else return d;
    }
    else {
        if(c > d)return c;
        else return d;
    }
}
else{
    if(b > c){
        if(b > d)return b;
        else return d;
    }
    else{
        if(c > d)return c;
        else return d;
    }
}
}
int main() 
{
    int a, b, c, d;
scanf("%d %d %d %d", &a, &b, &c, &d);
int ans = max_of_four(a, b, c, d);
printf("%d", ans);
return 0;
}
```
