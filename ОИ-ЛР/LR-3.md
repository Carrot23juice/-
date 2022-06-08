 Общая информатика

## Лабораторная работа №3


### Содержание

1. Задание
2. Текст программы
3. Описание работы программы

### 1. Задание
Написать программу, которая может считывать данные из файла, обрабатывать и выводить результат в другой файл. В данной работе я буду обрабатывать три значения вектора, искать его длину и выводить результат в файл.





### 2. Текст программы
```c++
#include <iostream>
#include <fstream>
#include <cmath>
using namespace std;

int main() 
{
	float a, b, c;
	ifstream ifile("D:/LR_3/input.txt");
	if (!(ifile.is_open))
	cout << "file is not open \n";

	ifile >> a >> b >> c;
	ifile.close();
	
	float d; 
	d = sqrt(a * a + b * b + c * c);
	
	ofstream ofile("D:/LR_3/output.txt");
	ofile << d;
	ofile.close(); 

	system("pause");
	return (0);
}
```
### 3. Описание работы программы
