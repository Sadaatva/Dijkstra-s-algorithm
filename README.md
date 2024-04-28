# Программа для вычисления кратчайших путей
Этот код реализует алгоритм поиска кратчайших путей во взвешенном графе с использованием алгоритма Дейкстры. Он находит кратчайшие расстояния от начальной вершины до всех остальных вершин в графе.

## Описание задачи:
Дан взвешенный граф с заданными весами ребер в виде матрицы смежности. Требуется найти кратчайшие расстояния от начальной вершины до всех остальных вершин в графе.

## Использование:
Программа запрашивает размер матрицы (количество вершин) и вводит матрицу смежности графа. Затем она применяет алгоритм Дейкстры для нахождения кратчайших расстояний от первой вершины до всех остальных. Результаты выводятся в виде кратчайших расстояний от первой вершины до каждой из остальных.

## Формат ввода:
Программа ожидает ввод от пользователя в следующем формате:
Пользователю предлагается ввести размер матрицы (количество вершин). Затем пользователь вводит саму матрицу смежности графа, где каждое число представляет вес ребра между соответствующими вершинами. Вес ребра должен быть 0 или положительным числом. Если вес ребра между двумя вершинами равен 0, это означает, что вершины не соединены.

# Функции:

1) `void main()`:
   
1.1 Ввод размера матрицы и создание массивов: Пользователю предлагается ввести размер матрицы (количество вершин). Затем создаются динамические массивы для матрицы смежности, массива кратчайших расстояний и массива, отслеживающего посещенные вершины.
   
1.2 Ввод матрицы смежности: Пользователю предлагается ввести матрицу смежности графа, где каждое число представляет вес ребра между соответствующими вершинами.

1.3 Применение алгоритма Дейкстры: Вызывается функция dijkstra(), которая выполняет алгоритм Дейкстры для нахождения кратчайших расстояний от первой вершины до всех остальных.

1.4 Вывод результатов: Кратчайшие расстояния от начальной вершины до всех остальных выводятся в консоль с помощью функции printShortestDistances().

1.5 Освобождение памяти: После завершения работы программы освобождается выделенная динамически память.

   
2) `void deleteMatrix(int** matrix, int size)`:
Эта функция освобождает память, выделенную для матрицы смежности графа.

3) `void printShortestDistances(int* distances, int size)`:
Функция выводит кратчайшие расстояния от начальной вершины до всех остальных вершин в графе.

4) `void dijkstra(int** matrix, int* distances, bool* visited, int size)`:
Функция реализует алгоритм Дейкстры для нахождения кратчайших расстояний от начальной вершины до всех остальных вершин в графе. Она обновляет массив кратчайших расстояний и массив посещенных вершин на каждой итерации.

5) `void initializeArrays(int** matrix, int* distances, bool* visited, int size)`:
Эта функция инициализирует массивы кратчайших расстояний и посещенных вершин перед выполнением алгоритма Дейкстры. Каждое расстояние устанавливается в бесконечность, а все вершины помечаются как непосещенные.

6) `void printMatrix(int** matrix, int size)`:
Функция выводит матрицу смежности графа в консоль. Каждый элемент матрицы выводится построчно, с разделением значений для каждой вершины.






