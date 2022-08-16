# 【CppSTL】打印数据结构



[toc]



## vector

```c++
#include <iostream>
#include <vector>

using namespace std;

template<class T>
void print_vector(vector<T>& v) {
	for (typename vector<T>::iterator it = v.begin(); it != v.end(); it++) {
		cout << *it << " ";
	}
	cout << endl;
}

int main() {
	vector<int> v1 = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
	print_vector(v1);

	vector<double> v2 = { 0.0, 1.1, 2.2, 3.3, 4.4, 5.5, 6.6, 7.7, 8.8, 9.9 };
	print_vector(v2);

	return 0;
}
```

运行结果：

```
0 1 2 3 4 5 6 7 8 9
0 1.1 2.2 3.3 4.4 5.5 6.6 7.7 8.8 9.9
```



```c++
#include <iostream>
#include <cstring>
#include <vector>

using namespace std;

template<class T>
void print_vector(vector<T>& v, string vector_name) {
	cout << vector_name << ": ";
	for (typename vector<T>::iterator it = v.begin(); it != v.end(); it++) {
		cout << *it << " ";
	}
	cout << endl;
}

int main() {
	vector<int> v1 = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
	print_vector(v1, "v1");

	vector<double> v2 = { 0.0, 1.1, 2.2, 3.3, 4.4, 5.5, 6.6, 7.7, 8.8, 9.9 };
	print_vector(v2, "v2");

	return 0;
}
```

运行结果：

```
v1: 0 1 2 3 4 5 6 7 8 9
v2: 0 1.1 2.2 3.3 4.4 5.5 6.6 7.7 8.8 9.9
```

