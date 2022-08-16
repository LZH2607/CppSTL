# 【CppSTL】vector



[toc]



## 一、头文件

```c++
#include <vector>
```



## 二、构造

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
	// 方式1
	vector<int> v1;
	for (int i = 0; i < 10; i++) {
		v1.push_back(i);
	}
	print_vector(v1, "v1");

	// 方式2
	vector<int> v2 = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
	print_vector(v2, "v2");

	// 方式3
	vector<int> v3(10, 1); // 10个1
	print_vector(v3, "v3");

	// 方式4
	vector<int> v4 = v1;
	print_vector(v4, "v4");

	// 方式5
	vector<int> v5(v1);
	print_vector(v5, "v5");

	// 方式6
	vector<int> v6(++v1.begin(), --v1.end());
	print_vector(v6, "v6");

	return 0;
}
```

运行结果：

```
v1: 0 1 2 3 4 5 6 7 8 9
v2: 0 1 2 3 4 5 6 7 8 9
v3: 1 1 1 1 1 1 1 1 1 1
v4: 0 1 2 3 4 5 6 7 8 9
v5: 0 1 2 3 4 5 6 7 8 9
v6: 1 2 3 4 5 6 7 8
```



## 三、插入



## 四、删除



