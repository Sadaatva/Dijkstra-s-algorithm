# Программа для вычисления кратчайших путей
Этот код реализует алгоритм поиска кратчайших путей во взвешенном графе с использованием алгоритма Дейкстры. Он находит кратчайшие расстояния от начальной вершины до всех остальных вершин в графе.

## Описание задачи:
Дан взвешенный граф с заданными весами ребер в виде матрицы смежности. Требуется найти кратчайшие расстояния от начальной вершины до всех остальных вершин в графе.

## Использование:
Программа запрашивает размер матрицы (количество вершин) и вводит матрицу смежности графа. Затем она применяет алгоритм Дейкстры для нахождения кратчайших расстояний от первой вершины до всех остальных. Результаты выводятся в виде кратчайших расстояний от первой вершины до каждой из остальных.

## Формат ввода:
Программа ожидает ввод от пользователя в следующем формате:
Пользователю предлагается ввести размер матрицы (количество вершин). Затем пользователь вводит саму матрицу смежности графа, где каждое число представляет вес ребра между соответствующими вершинами. Вес ребра должен быть 0 или положительным числом. Если вес ребра между двумя вершинами равен 0, это означает, что вершины не соединены.

# Решение

1. **Инициализация**: Создаются необходимые переменные и выделяется память под матрицу смежности графа, массив кратчайших расстояний и массив посещенных вершин.

2. **Ввод данных**: Пользователю предлагается ввести размер матрицы (число вершин графа) и саму матрицу смежности графа. Элементы матрицы должны быть целыми числами, представляющими веса рёбер. Веса должны быть неотрицательными. Если между вершинами нет ребра, вводится 0 или любое другое значение, которое обозначает отсутствие ребра.

3. **Инициализация расстояний и посещенных вершин**: Все расстояния от начальной вершины до остальных исходно устанавливаются как бесконечность, а все вершины помечаются как непосещенные. Расстояние от начальной вершины до самой себя устанавливается равным 0.

4. **Поиск кратчайших путей**: Повторяем следующий шаг `size - 1` раз, где `size` - количество вершин графа.
   - Находим вершину с наименьшим расстоянием от начальной вершины среди непосещенных.
   - Помечаем эту вершину как посещенную.
   - Обновляем расстояния до всех смежных вершин через выбранную вершину, если новое расстояние меньше текущего.

5. **Вывод результатов**: После завершения алгоритма выводятся кратчайшие расстояния от начальной вершины до всех остальных.

6. **Освобождение памяти**: После завершения работы программы освобождается выделенная память.
