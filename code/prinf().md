```
#include<iostream>
using namespace std;

class printDate
{
	public:
	void print(int i)
	{
		cout << "integer：" << i << endl;
	}
	
	void print(double f)
	{
		cout << "float:" << c << endl;
	}
	
	void print(char c[])
	{
		cout << "character:"  << c <<endl;
	}
}

int main()
{
	printDate pd;
	pd.print(5);
	pd.print(5.0);
	pd.print("5");

	return 0;
}
```

