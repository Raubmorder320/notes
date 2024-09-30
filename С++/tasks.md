### sort

#### 1,2,3
Нарисуйте сеть сортировки (для небольшого количества сравниваемых чисел) для алгоритмов:
сортировкa пузырьком, сортировка вставками, сортировка отбором 
 
#### 4
Написать функцию, принимающую в качестве параметров три массива. Предполагается, что первые два массива упорядочены в порядке возрастания. Функция должна формировать третий массив из первых двух массивов таким образом, чтобы он тоже был упорядоченным.

```C
void sort_4(int arr1[], int n1, int arr2[], int n2, int arr3[]) {
  int i = 0, j = 0, k = 0;

  // Сравниваем элементы из обоих массивов и добавляем меньший в arr3
  while (i < n1 && j < n2) {
    if (arr1[i] <= arr2[j]) {
      arr3[k++] = arr1[i++];
    } else {
      arr3[k++] = arr2[j++];
    }
  }

  // Добавляем оставшиеся элементы из arr1, если они есть
  while (i < n1) {
    arr3[k++] = arr1[i++];
  }

  // Добавляем оставшиеся элементы из arr2, если они есть
  while (j < n2) {
    arr3[k++] = arr2[j++];
  }
}

```

### search

#### 2
Реализовать алгоритм двоичного поиска как функцию с параметрами массив целых чисел, его длина и целое число x. Функция должна анализировать средний элемент массива, сравнивая его с x и сужая диапазон поиска соответствующим образом, до тех пор, пока либо не будет найден элемент, равный x (в этом случае возвращается его индекс), либо интервал поиска не станет вырожденным (в этом случае такого элемента нет, и нужно возвратить -1).

```C
int search_2a(int arr[], int length, int num) {
  int left = 0;
  int right = length - 1;

  while (left <= right) {
    int mid = left + (right - left) / 2; 

    if (arr[mid] == num) {
      return mid; // Элемент найден, возвращаем его индекс
    }

    if (arr[mid] < num) {
      left = mid + 1; // Ищем в правой половине
    } else {
      right = mid - 1; // Ищем в левой половине
    }
  }

  return -1; // Элемент не найден
}
```

```C
int search_2b(int arr[], int left, int right, int x) {
  if (right >= left) {
    int mid = left + (right - left) / 2;

    if (arr[mid] == x) {
      return mid; 
    }

    if (arr[mid] > x) {
      return search_2b(arr, left, mid - 1, x);
    }

    return search_2b(arr, mid + 1, right, x);
  }

  return -1;
}

```

#### 5
То же самое, но нужно вывести индекс первого вхождения искомого элемента в массив

```C
int search_5(int arr[], int length, int num) {

int left = 0;

int right = length - 1;

  

while (left <= right) {

int mid = left + (right - left) / 2;

  

if (arr[mid] == num) {

right = mid;

if ( arr[mid-1]!=num || mid == 0){

return mid; // Элемент найден, возвращаем его индекс

}

// Элемент найден, возвращаем его индекс

}

  

if (arr[mid] < num) {

left = mid + 1; // Ищем в правой половине

} else {

right = mid - 1; // Ищем в левой половине

}

}

  

return -1; // Элемент не найден

}
```

### strings

#### 1
Ввести имя файла, возможно, содержащее путь, и вывести:
a) имя последней папки в пути (без циклов).

```C
void str_1(){

char s[] = "C:/ubuntu/is/the/best.h";

int length = sizeof(s)/sizeof(char);

char* start = s;

char* symbol = strrchr(s, '/');

int slash = symbol - start;

char s2[slash+1];

strncpy(s2, s, slash);

s2[slash] = '\0';

char* start2 = s2;

char* symbol2 = strrchr(s2, '/');

int slash2 = symbol2 - start2 + 1;

getString(slash2, slash+1, s2);

}
```

b) имя файла с путем, но расширение заменено на html (без циклов)

```C
void str_1b(){

char s[] = "C:/ubuntu/is/the/best.h";

int length = sizeof(s)/sizeof(char);

char* startp = s;

char* dotp = strrchr(s, '.');

int dot = dotp - startp + 1;

char s2[dot+5];

strncpy(s2, s, dot);

s2[dot] = '\0';

strcat(s2, "html");

puts(s2);

}
```

#### 2
Написать функцию, принимающую в качестве параметров две строки и
возвращающую число вхождений второго параметра в первый. Рассмотреть
случаи:
а) вхождения могут перекрываться
```C
```

б) не могут перекрываться.
```C
```
