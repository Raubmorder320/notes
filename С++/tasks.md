## C
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
int getString(int pos, int len, char string[]) //функция для взятия среза от pos до конца строки

{

int i = 0;

char substring[1000];

  

while (i < len) {

substring[i] = string[pos + i - 1];

i++;

}

substring[i] = '\0';

puts(substring);

return 0;

}



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
int str_2a(char* str, char* sub) {

int count = 0; //счетчик

int len = strlen(sub);

for (int i = 0; i <= strlen(str) - len; i++) { //цикл от начала строки до длины строки минус длина образца

if (strncmp(str + i, sub, len) == 0) { //условие сравнивает срез строки с образцом с помощью арифметики указателей

count++;

}

}

return count;

}
```

б) не могут перекрываться.
```C
int str_2b(char* str, char* sub) {

int count = 0; //счетчик

int len = strlen(sub);

int i = 0;

int length = strlen(str);

while (i<=length){

if (strncmp(str + i, sub, len) == 0) { //условие сравнивает срез строки с образцом с помощью арифметики указателей

count++;

if (i+len<=length){ //проверка, можно ли перепрыгнуть на конец найденного образца, чтобы избежать перекрытий

i+=len;

continue;

}

}

i++;

}

  

return count;

}
```

#### 3 

Написать функцию, принимающую в качестве параметров две строки и
возвращающую копию первого параметра, из которой удалено первое
вхождение второго параметра (без циклов).
```C
char* str_3(char* str, char* sub){

int len = strlen(sub);

char* enter = strstr(str, sub); //указатель на первое вхождение образца

char* res = (char*)malloc(strlen(str) - len);

strncpy(res, str, (int)(enter - str)); //копируем все от начала до первого вхождения

strncat(res, enter+len, strlen(str)); //складываем с тем что после найденного вхождения

return res;

}
```



### structures
#### машины
1) написать структурный тип данных, описывающий автомобиль и написать функции, принимающие массив автомобилей и делающие следующее:
2) Инициализация. У каждого автомобиля из массива дополнительное логическое поле устанавливается в false, что означает, что массив пока пуст
3) Заполнение склада. Пробежаться по массиву и для каждой ячейки, логическое поле которой имеет значение false, сделать следующее: ввести с клавиатуры значения полей, и логическое поле установить в true.
4) Печать информации. Пробежаться по массиву и для каждой ячейки, логическое поле которой имеет значение true, напечатать номер в массиве и информацию о соответствующем автомобиле.
5) Продать автомобиль. Ввести с клавиатуры его номер в массиве и проверить, что автомобиль с указанным номером имеется на складе, т. е. у соответствующего элемента массива логическое поле имеет значение true. Если это так, то продать автомобиль, т. е. установить его логическое поле в false. Иначе выдать сообщение об ошибке.
6) В функции main завести массив из 10 автомобилей, и организовать цикл, на каждой итерации которого пользователю выдается меню из пяти пунктов (четыре вышеописанных функции и выход из программы), вводится выбор пользователя и вызывается выбранная пользователем функция, до тех пор, пока пользователь не выберет выход.


```c
//struct cars

struct car{

int value;

char color[100];

double power;

bool available;

};

  

void initialization(struct car cars[]){

for (int i=0; i < 10; i++){

cars[i].available = false;

}

}

  

void fillStorage(struct car cars[]) {

for (int i = 0; i < 10; i++) {

printf("Введите цену автомобиля\n"); scanf("%d", &cars[i].value);

printf("Введите мощность автомобиля\n"); scanf("%lf", &cars[i].power);

printf("Введите цвет автомобиля\n"); scanf("%s", cars[i].color);

cars[i].available = true;

}

}

  

void information(struct car cars[]){

for (int i = 0; i < 10; i++){

if(cars[i].available){

printf("Цена: %d\n Цвет: %s\n Мощность: %lf\n", cars[i].value, cars[i].color, cars[i].power);

}

}

}

  

void sale(struct car cars[]){

for (int i = 0; i < 10; i++){

if (cars[i].available){

cars[i].available = false;

}

}

}
```

### unions
Написать структурный тип данных, который может представлять вещественное или целое число. Должны быть реализованы функции, обеспечивающие арифметические операции и операции сравнения.

```c
typedef enum{

type_real, type_int

} type;

  

union inouble{

int integer;

double real;

};

  

struct var{

union inouble value;

type type;

};

struct var id_operation(struct var a, struct var b, char flag){

struct var result;

switch (flag) {

case '+':

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

result.value.integer = a.value.integer + b.value.integer;

break;

case type_real:

result.value.real = a.value.integer + b.value.real;

break;}

break;

case type_real:

switch (b.type)

{case type_int:

result.value.real = a.value.real + b.value.integer;

break;

case type_real:

result.value.real = a.value.real + b.value.real;

break;}

break;

}

break;

case '-':

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

result.value.integer = a.value.integer - b.value.integer;

break;

case type_real:

result.value.real = a.value.integer - b.value.real;

break;}

break;

case type_real:

switch (b.type)

{case type_int:

result.value.real = a.value.real - b.value.integer;

break;

case type_real:

result.value.real = a.value.real - b.value.real;

break;}

}

break;

case '*':

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

result.value.integer = a.value.integer * b.value.integer;

break;

case type_real:

result.value.real = a.value.integer * b.value.real;

break;}

break;

case type_real:

switch (b.type)

{case type_int:

result.value.integer = a.value.real * b.value.integer;

break;

case type_real:

result.value.real = a.value.real * b.value.real;

break;}

}

break;

case '/':

if (abs(b.value.real) < 10e-6 || b.value.integer != 0)

{

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

result.value.real = (double)a.value.integer / (double)b.value.integer;

break;

case type_real:

result.value.real = (double)a.value.integer / b.value.real;

break;

}

break;

case type_real:

switch (b.type)

{case type_int:

result.value.real = a.value.real / (double)b.value.integer;

break;

case type_real:

result.value.real = a.value.real / b.value.real;

break;

}

}

break;}

else{

printf("Деление на ноль\n");

}

};

  

return result;

}

  
  

bool id_compare(struct var a, struct var b, char flag){

switch (flag){

case '<':

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

return a.value.integer < b.value.integer;

break;

case type_real:

return a.value.integer < b.value.real;

break;}

break;

case type_real:

switch (b.type)

{case type_int:

return a.value.real < b.value.integer;

break;

case type_real:

return a.value.real < b.value.real;

break;}

}

break;

case '>':

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

return a.value.integer > b.value.integer;

break;

case type_real:

return a.value.integer > b.value.real;

break;}

break;

case type_real:

switch (b.type)

{case type_int:

return a.value.real > b.value.integer;

break;

case type_real:

return a.value.real > b.value.real;

break;}

}

break;

case '=':

switch(a.type){

case type_int:

switch (b.type)

{case type_int:

return a.value.integer == b.value.integer;

break;

case type_real:

return a.value.integer == b.value.real;

break;}

break;

case type_real:

switch (b.type)

{case type_int:

return a.value.real == b.value.integer;

break;

case type_real:

return abs(a.value.real - b.value.real) < 10e-6;

break;}

}

break;

}

}
```

### input-output
#### 43.1
Написать программу, которая выводит в текстовый файл "f.txt" таблицу значений sin(x) для x, меняюще-
гося от 0 до 1 с шагом 0.1. Первая строка этой таблицы должна быть заголовком вида "x sin(x)".

```c
int sinus(){

FILE* fp = fopen("sin.txt", "w");

if (fp == NULL){

return -1;

}

fprintf(fp, "x sin(x)\n");

for (double i = 0; i < 11; i++){

  

fprintf(fp, "%.1f %.6lf\n", i/10, sin(i/10));

};

  

fclose(fp);

}
```

#### 43.2
Написать программу, считывающую из текстового файла "g.txt" фамилии абитуриентов и их оценки по

математике и физике и выдающую на экран таблицу, содержащую фамилии и сумму баллов за оба экзамена. Рас-
смотреть два случая:

а) формат данных во входном файле "g.txt" представлен следующим примером:
Иванов 5 5
Петров 4 5
Алексеев 5 4
...
б) Кроме данных в формате пункта а) входной файл содержит первую строку заголовка, имеющую вид "Фамилия
математика физика".
(решение представлено для б)

```c
int exam(){

FILE* ep = fopen("exam.txt","r");

FILE* fp = fopen("f.txt","w");

if (fp == NULL)

return -1;

char str[256];

int x, y;

fscanf(ep, "%s", str);

fscanf(ep, "%s", str);

fscanf(ep, "%s", str);

while (fscanf(ep, "%s", str) == 1){

fscanf(ep, "%d", &x);

fscanf(ep, "%d", &y);

fprintf(fp, "%s %d\n", str, x+y);

}

  

fclose(fp);

}
```

#### 43.3
Написать функцию, принимающую две строки и копирующую файл с именем, заданным первой строкой,
в файл, имя которого задано второй строкой. Старое содержимое последнего файла, если такой был, удаляется.

```c
int exam(){

FILE* ep = fopen("exam.txt","r");

FILE* fp = fopen("f.txt","w");

if (fp == NULL)

return -1;

char str[256];

int x, y;

fscanf(ep, "%s", str);

fscanf(ep, "%s", str);

fscanf(ep, "%s", str);

while (fscanf(ep, "%s", str) == 1){

fscanf(ep, "%d", &x);

fscanf(ep, "%d", &y);

fprintf(fp, "%s %d\n", str, x+y);

}

  

fclose(fp);

}
```

## C++

### vectors

#### 1.
Написать шаблонную функцию enlarge, принимающую вектор по ссылке и вставляющую между каждыми соседними элементами их полусумму.
```c++
void enlarges(vector <int> & v)

{

vector <int>::iterator i;

for (i = v.begin() + 1; i != v.end() ; i++){

i = v.insert(i,(*(i)+*(i-1))/2);

++i;

}

  

}
```

#### 2.

Написать шаблонную функцию del, принимающую вектор по ссылке и удаляющую элементы вектора через один.

```c++
void del(vector <int> & v){

// vector <int>::iterator i;

for(int i = 0; i < size(v); i++){

v.erase(v.begin()+i);

}

}
```

#### 3.

В функции main завести вектор и инициализировать его списком

значений элементов. Завести также массив из такого же числа элементов. При помощи алгоритма copy переписать содержимое вектора в массив и вывести элементы массива.

```c++
vector <int> concat(vector <int> v1, vector <int> v2){

vector <int> v3(size(v1)+ size(v2));

copy(v1.begin(), v1.end(), v3.begin());

copy(v2.begin(),v2.end(),v3.begin()+size(v1));

return v3;

}
```

#### 4.

Написать шаблонную функцию concat, принимающую два вектора и
возвращающую их сцепление (сначала идут элементы первого, а затем второго).

```c++
vector <int> concat(vector <int> v1, vector <int> v2){

vector <int> v3(size(v1)+ size(v2));

copy(v1.begin(), v1.end(), v3.begin());

copy(v2.begin(),v2.end(),v3.begin()+size(v1));

return v3;

}
```

#### 5.

Написать шаблонную функцию repeat, принимающую вектор v и

неотрицательное целое число n, и возвращающую новый вектор, полученный повторением вектора v n раз.

```c++
vector <int> repeat(vector <int> v, int n){

vector <int> v_ext(size(v)*n);

for (int i = 0; i<=n; i++){

copy(v.begin(), v.end(), v_ext.begin()+i*size(v));

}

return v_ext;

}
```

#### 6.

Написать функцию second_occure, находящую второе вхождение данного значения в заданный вектор, если оно там есть, и вернуть итератор конца
вектора, если его там нет (без циклов!).

```c++
vector <int>::iterator second_occure(vector <int> v, int x){

vector <int>::iterator i;

i = find(v.begin(), v.end(), x);

if (i!= v.end()){

return find(i+1, v.end(), x);

}

else return i;

}
```

#### 10.

Написать функцию, принимающую упорядоченный вектор из вещественных чисел, вещественное число x и две целые переменные i и j по ссылке.
Функция должна определять пару индексов соседних элементов вектора, между которыми лежит x. Если элемента, равного x, в векторе нет, индексы i и j будут
различны. Если элемент есть – индексы будут одинаковы (оба они равны индексу
искомого элемента).

```c++
void is_occure(vector <double> v, double x, int &i, int &j){

vector <double>::iterator it_i;

vector <double>::iterator it_j;

it_i = lower_bound(v.begin(),v.end(),x);

it_j = upper_bound(v.begin(),v.end(),x)-1;

i = distance(v.begin(),it_i);

j = distance(v.begin(),it_j);

}
```

### strings in cpp style

#### 1. 

Напишите функцию, которая проверяет, является ли переданная ей строка правильным IP-адресом.

```c++
int is_right_ip(string str){

int c = 0;

for (int j = 0; j<3;j++){

int i = str.find_last_of('.');

if (i != string::npos){

int ip = stoi(str.substr(i+1));

if (ip>0 && ip<256){

c++;

}

str.erase(i);

}

}

if (c==3 && stoi(str) > 0 && stoi(str) < 256){

return 1;

}

return 0;

}
```

#### 2.

Написать функцию, принимающую в качестве параметров две строки и возвращающую копию первого параметра, все вхождения второго пара-
метра в которой взяты в «()», т. е., например, если параметрами были строки
ertabcsdftyuabczevbh и abc, то вернуть надо ert(abc)sdftyu(abc)zevbh.

```c++
string insert_pattern(string str, string pattern){

int i = 0;

string new_str = str;

while (str.find(pattern, i) != string::npos){

int pattern_index = str.find(pattern, i);

str.insert(pattern_index, 1, '(');

str.insert(pattern_index + pattern.size() + 1,1, ')');

i += pattern_index+pattern.size();

}

return str;

}
```

#### 3.

Ввести строку и заменить все встречающиеся в ней суммы натуральных чисел на их результаты. Например, если есть строка 5+26-72+35gh32+45,

результат должен быть 31-107gh77.