```cpp
int input(int a[], int n)
{
    for(int i=0; i<n ; i++)
    {
        cout<<"a["<<i<<"]=";
        cin>>a[i];
    }
}
int output(int a[], int n)
{
    for( int i=0; i<n ; i++)
    {
        cout<<a[i]<<" ";
    }
}
void ranger(int a[], int n)
{
    int k=0;
    for(int i=0; i<n-1; i++)
    {
        for( int j=i+1; j<n ; j++)
        {
            if(a[i]>a[j])
            {
                k=a[i];
                a[i]=a[j];
                a[j]=k;
            }
        }
    }
}
int inserer(int a[], int &n , int vitricanchen, int x)
{
    for(int i=n; i>=vitricanchen; i--)
    {
        a[i]=a[i-1];
    }
    a[vitricanchen]=x;
    n++;
}

int main()
{
    int a[100];
    int n,x, vitricanchen;
    cout<<" entrez n";
    cin>>n;
    cout<<" entrez le tableau "<<endl;
    input(a, n);
    cout<<" imprimez le tableau "<<endl;
    output(a, n);
    ranger(a,n);
    cout<<" faites la range des numero ";
    output(a, n);
    cout<<" entrez x";
    cin>>x;
    cout<<" entrez vitricanchen";
    cin>>vitricanchen;
    inserer(a,n,vitricanchen,x);
    cout<<" rangez apres d'inserer le x ";
    ranger(a,n);
    output(a, n);

}
```
