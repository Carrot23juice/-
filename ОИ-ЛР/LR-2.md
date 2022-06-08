# Общая информатика

## Лабораторная работа №2

### Содержание

1.Задание
2.Код
3.Описание работы программы

### 1. Задание

Написать прогамму способную умножить две матрицы, используя статический массив.


### 3. Текст программы

```c++
#include <iostream>

using namespace std;

int main () {
	const int N = 4,  M = 2, K = 3;		//Объявление количества сторк и столбцов
	int A[N][M], B[M][K], C[N][K];		//Объявление матриц

	cout << "Write Values of Matrix A" << endl;
	for (int i=0; i<N; i++)		//Цикл для задания чисел в первой матрице
	{
		for (int j=0; j<M; j++)
		{
			cout << "A["<<i+1<<"], ["<<j+1<<"]=";
			cin >> A[i][j];
		}
	}

	cout << "Write Values of Matrix B" << endl;
	for (int x=0; x<M; x++)		//Цикл для задания чисел во второй матрице
	{
		for (int y=0; y<K; y++)
		{
			cout <<"B["<<x+1<<"], ["<<y+1<<"]=";
			cin >> B[x][y];
		}
	}

	cout << "Matrix A" << endl;		//Вывод первой матрицы
	for (int i=0; i<N; i++)
	{
		for (int j=0; j<M; j++)
		{
			cout << A[i][j] << " ";
		}
		cout << endl;
	}
	
	cout << "Matrix B" << endl;//Вывод второй матрицы
	for (int x=0; x<M; x++)
	{
		for (int y=0; y<K; y++)
		{
			cout << B[x][y] << " ";
		}
		cout << endl;
	}


	for (int i=0; i<N; i++)			//Расчет матрицы
	{
		for (int j=0; j<K; j++)
		{
			C[i][j]=0;
			for (int k=0; k<M; k++)
			{
				C[i][j]+=A[i][k]*B[k][j];
			}
		}
	}
	
	cout << "Matrix C" << endl;
	for (int i=0; i<N; i++)		//Вывод расчитанной матрицы
	{
		for (int j=0; j<M; j++)
		{
			cout << C[i][j] << " ";
		}
		cout << endl;
	}
	system ("pause");
	return 0;
}
```

### 4. Описание работы программы

