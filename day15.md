1, You have to complete the function void update(int *a,int *b), which reads two integers as argument, and sets a with the sum of them, and  with the absolute difference of them.


```cpp
void update(int *a,int *b) {
    // Complete this function  
    *a += *b;
    *b= 2*(*b)-*a;
    *b= *b>0 ? *b : -1*(*b);
    
};

int main()
{
    int a, b;
    int *pa = &a, *pb = &b;
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
```
2.The first line contains two space-separated integers denoting the respective values of  (the number of variable-length arrays) and  (the number of queries).
Each line  of the  subsequent lines contains a space-separated sequence in the format k a[i]0 a[i]1 … a[i]k-1 describing the -element array located at .
Each of the  subsequent lines contains two space-separated integers describing the respective values of  (an index in array ) and  (an index in the array referenced by ) for a query.
```cpp
int n, q;
	cout<<"nhap n,q";
	cin >> n >> q;

	// create 2D array
	int** a = new int*[n]();

	// fill 2D array with 1D subarrays
	for (int i = 0; i < n; i++) {
		// get the length of the 1D array at a[i]
		int k;
		cout<<"nhap k";
		cin >> k;

		// create the 1D subarray with the given length
		int* i_arr = new int[k]();

		// fill the subarray with k values
		for (int j = 0; j < k; j++) {
                cout<<"nhap day:";
			cin >> i_arr[j];
		}

		// store the subarray in a
		a[i] = i_arr;
	}



	for (int q_num = 0; q_num < q; q_num++) {

		int i, j;
		cout<<"nhap i,j"<<endl;
		cin >> i >> j;
		cout << a[i][j] << endl;
	}

	for (int i = 0; i < n; i++) {
		delete[] a[i];
	}
	delete[] a;

	return 0;
}
```
