# Ответы на вопросы из 5 теста Чабанова

## Вопросы
1) Выберите все выражения, которые не вызовут ошибку, при условии, что переменная a объявлена как: <code>int a = 4;</code><br>

Ответ: <code> int& r1 = a; </code><br>
<code> int&& r4 = a + 1; </code><br>
<code> int& r5 = r1; </code><br>
<code> int& r7 = r4; </code>

2) Как обозначается r-value ссылка на значение типа int в С++?<br>

Ответ: <code> int&& </code><br>

3) Как обозначается r-value ссылка на значение типа int в С++?
```cpp
class A{
public:
    int value = 1;
    void set_value(int value){
        this->value = value;
    }
};

class B: public A{
public:
    int value = 1;
    void set_value(int value){
        this->value = value;
    }
};

B obj;
obj.set_value(5);
std::cout << obj.value;
```
Ответ: <code> 5 </code>

4) Что такое горутина в Go?<br>

Ответ: <code> Легковесный поток выполнения </code>

5) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    ~A(){
        std::cout << 'A';
    }
};

class B{
public:
    ~B(){
        std::cout << 'B';
    }
};

class C: public A, public B{
public:
    ~C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ: <code> CBA </code>

6) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
};

C obj;
obj.get();
```
Ответ: <code> Ошибка </code>

7) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    int value = 1;
    B(int value){
        this->A::value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

8) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    A(){
    	value = 5;
    }
    A(int value){
    	value = 9;
    }
};

class B: public A{
public:
    B(int value):A(value){};
};

B obj(1);
std::cout << obj.value;
```
Ответ: <code> 1 </code>

9) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    ~A(){
        std::cout << 'A';
    }
};

class B{
public:
    ~B(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    ~C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ: <code> CAB </code>

10) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    void set_value(int value){
        this->value = value;
    }
};

class B: public A{
public:
    int value = 1;
};

B obj;
obj.set_value(5);
std::cout << obj.value;
```
Ответ: <code> 1 </code>

11) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    void get(){
        std::cout << 'C';
    }
};

C obj;
obj.get();
```
Ответ: <code> C </code>

12) Что из перечисленного является объявлением конструктора копирования класса <code>SomeClass</code>?<br>

Ответ: <code> SomeClass(const SomeClass& other); </code>

13) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
};

class C: public B, public A{
};

C obj;
obj.get();
```
Ответ: <code> A </code>

14) Как заблокировать мьютекс в Go?<br>

Ответ: <code> mutex.Lock() </code>

15) Что такое мьютекс в Go?<br>

Ответ: <code> Механизм синхронизации доступа горутин к общим ресурсам </code>

16) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: private A{
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

17) Дан фрагмент кода на языке С++. Какой модификатор доступа у <code>valueA</code> в классе <code>B</code> ?
```cpp
class A{
private:
    int valueA = 1;
};

class B: public A{
public:
    int valueB = 5;
};
```
Ответ: <code> поле не доступно </code>

18) Что из перечисленного является объявлением конструктора перемещения класса <code>SomeClass</code>?<br>

Ответ: <code> SomeClass(SomeClass&& other); </code>

19) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    A(int value){
        this->value = value;
    }
    int value = 1;
};

struct B: A{
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

20) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    A(){
        std::cout << 'A';
    }
};

class B{
public:
    B(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ: <code> Ничего </code>

21) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    void get(){
        B::get();
    }
};

C obj;
obj.get();
```
Ответ: <code> B </code>

22) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    B(int value){}
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> 1 </code>

23) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    A(){
    	value = 5;
    }
    A(int value){
    	this->value = 9;
    }
};

class B: public A{
public:
    B(int value):A(value){};
};

B obj(1);
std::cout << obj.value;
```
Ответ: <code> 9 </code>

24) Как запустить горутину в Go?<br>

Ответ: <code> go funcName() </code>

25) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    A(){
        std::cout << 'A';
    }
};

class B{
public:
    B(){
        std::cout << 'B';
    }
};

class C: public A, public B{
public:
    C(){
        std::cout << 'C';
    }
};

C obj();
```
Ответ: <code> Ничего </code>

26) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
};

class B{
public:
    int value = 5;
};

class C: public A, public B{
public:
    int value = 9;
};

C obj;
std::cout << obj.value;
```
Ответ: <code> 9 </code>

27) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> 5 </code>

28) Что будет выведено на экран в результате работы этого кода?
```cpp
#include <iostream>

void foo(int& a){
    std::cout << "+" << std::endl;
}

void foo(int&& a){
    std::cout << "-" << std::endl;
}

int main(){
    int a = 4;
    foo(a + 1);
}
```
Ответ: <code> - </code>

29) Как разблокировать мьютекс в Go?<br>

Ответ: <code> mutex.Unlock() </code>

30) Дан фрагмент кода на языке С++. Какой модификатор доступа у <code>valueA</code> в классе <code>B</code> ?
```cpp
class A{
public:
    int valueA = 1;
};

class B: private A{
public:
    int valueB = 5;
};
```
Ответ: <code> private </code>

31) Как обозначается l-value ссылка на значение типа int в С++?<

Ответ: <code> int& </code>

32) Дан фрагмент кода на языке С++. Какой модификатор доступа у <code>valueA</code> в классе <code>B</code> ?
```cpp
struct A{
    int valueA = 1;
};

class B: protected A{
public:
    int valueB = 5;
};
```
Ответ: <code> protected </code>
