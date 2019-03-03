# Name:
Marina Lianskaya
# Contacts:
* *phone:* +375447574680;
* *skype:* marina.lianskaya;
* *email:* marinalianskaya@gmail.com
# Summary:
I am junior software developer. I like Front-end development and I really like nice UI/UX.
Always try to self-educate. I would like to develop my skills in that direction.
# Skills:
* C++ 
* html
* CSS
* JS
* React
* Angular
* jQuery
# Code examples:
```c++
#include "stdafx.h" 
#include "iostream" 
#include <conio.h> 
using namespace std;

int main()
{
	setlocale(LC_ALL, "rus");
	int n, sum = 0;
	cout << "Введите aразмер двумерного массива" << endl;
	cin >> n;
	int **A = new int*[n];

	for (int i = 0; i < n; i++) {
		A[i] = new int[n];
	}

	cout << "Дайте значения данному массиву" << "\n";

	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++) {
			 A[i][j]= rand()%50-24;
			 cout << A[i][j];

		}
		cout << endl;
	}

	
	for (int i = 0; i < n - i; i++)
		for (int j = 0; j < n; j++)
		{
			int temp = A[i][j];
			A[i][j] = A[n - i - 1][n - j - 1];
			A[n - i - 1][n - j - 1] = temp;
		}

	cout << "Перевернутая матрица" << endl;
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++) {
			cout << A[i][j] << " ";
		}
		cout << "\n";
	}

	for (int i = 0; i < n; i++) {
		delete[] A[i];
	
	}
	delete[] A;
	system("pause");
	return 0;
}
```

```c++
#include "stdafx.h"
#include <iostream>
#include <cmath>
#include <iomanip>

using namespace std;

typedef double(*func) (double, double);

double func_s(double x, double n) {
		 double r=1, sum = 1;
		for (int k = 1; k <= n; k++) {
			r *= x * x / k;
			sum += r*(2 * k - 1)*x*x;
		}
		return sum;
}

double func_y(double x, double n) {
	return (1 + 2 * x * x) * exp(x * x);
}

double func_fabs(double x, double n) {
	return fabs(func_y(x, n) - func_s(x, n));
}

void rez(func f, double x, double b, double h, double n) {
	for (x; x < b; x += h) {
		cout << fixed << "x = " << x << setw(20) << "function: " << f(x, n) << endl;
	}
}

int main()
{
	double a = 0.1, b = 1, h = 0.1, x, n;
	x = a;
	cout << "enter n: ";
	cin >> n;
	cout << "1. S(x)\n2. Y(x)\n3. |Y(x)-S(x)|";
	int k;
	cin >> k;
	switch (k) {
	case 1: 
		cout << "Function = S(x)" << endl;
		rez(func_s, x, b, h, n);
		cout << endl;
		break;
	case 2:
		cout << "Function = Y(x)" << endl;
		rez(func_y, x, b, h, n);
		cout << endl;
		break;
	case 3:
		cout << "Function = |Y(x)-S(x)|" << endl;
		rez(func_fabs, x, b, h, n);
		cout << endl;
		break;
	default: cout << "again please";
	}
	system("pause");
    return main();
}
```

# Experience:
* html-academy
* codeacademy
* played with html/css/js
# Education: 
* University
* Youtube
* Conferences 
# Languages:
* *Russian* - Native
* *German* - B1 (lerned in school end in university)
* *English* - A2 (currently attending courses, read books and documentation)

 
 