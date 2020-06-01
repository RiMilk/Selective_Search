# Выборочный поиск

В данном проекте рассмотрено длва метода выборочного поиска:

  - Метод, основанный на обноружении границ

  - Метод, основанный на алгоритме П. Фельзенцвальба и Д. Хаттенлохера
  
  
#### Входные данные

Изображение формата .jpg .jpeg .png. (Путь к изображению или измененное изображение в папке ..\Assets\Input)

#### Выходные данные

Изображение формата .jpg (опционально) с отрисованными контурами (Опционально в папке ..\Assets\Output)

## Обнаружение границ

  - BinaryImage - Класс для изображений. Если исходное изображение не является бинарным, то преобразует его в нужно.
На вход подается матрица класса Mat, либо путь к изображени.

  - GetAllContours() - Найти все контуры на изображении и передаются в виде списка векторов. 
На вход поступает переменная типа BinaryImage. Результатом является список контуров типа VectorOfVectorOfPoint.

  - SortContours - Отсортировать контуров по принципу площади и колличества точек (что бы избежать контуров в виде точек)
  На вход поступает список контуров. Результатом является список отсортированных контуров.
  
  - GetRectangle - Получить всех прямоугольников, в которых есть выделенные контура. В дальнейшем области изображения из них можно передать на вход алгоритму классификации изображений. (Полностью расписано в проекте Classification_Of_CharactersIn_The_Scheme)
  На вход поступает список контуров. Результатом является список типа Rectangle.
  
  - DelineationOfRectangles - Нарисовать все прямоугольники на изображении и сохранить(по выбору) результат.
  На вход пуступает изображения типа Mat, список боксов, а так же (опционально) путь по которому надо сохранить изображение. Результатом является изображение с отрисованными на нем областями.
  
### Для чего?

Данный метод подходит для схем и данных изображений данного типа. Если использовать его для фотографий и изображений, где нет четких границ, а так же изображений не 2D формата, то есть шанс, что будут выделены не все нужные области.

## Метод на основе алгоритма П. Фельзенцвальба и Д. Хаттенлохера

(В разработке)
