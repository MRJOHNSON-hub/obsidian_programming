[C++ Data Types](https://www.w3schools.com/cpp/cpp_data_types.asp)

| type                      | size                | range             | type              | size | range             |
| ------------------------- | ------------------- | ----------------- | ----------------- | ---- | ----------------- |
| int                       | 4                   | -2*10^9 to 2*10^9 | short int (short) | 2    | -32768 to 32768   |
| float (7 after decimal)   | 4                   |                   | long long int     | 8    | كتيير             |
| double (15 after decimal) | 8                   |                   | unsigned  int     | 4    | 1 to 4*10^9 (+ve) |
| char                      | 1                   |                   | unsigned  char    | 1    | +ve ascii         |
| bool                      | 1                   |                   |                   |      |                   |
| string                    | 32                  |                   |                   |      |                   |
| array                     | depend on the array |                   |                   |      |                   |
> تقدر تعرف var من غير ما تقول نوعه وتخليه يستنتجه عن طريق تحط كلمة auto بس لازم تديله قيمة

```c++
int num=10;
cout<<"sizeof(num)";
cout<< &num; // print memory location
```

---
## integer:
> عند وضع true or false مع int يعطي 1, 0
> عند وضع fraction لمتغير int يتجاهل ال decimal
``` c++
#include <limits.h>
cout<< INT_MIN<<INT_MAX;

```

--- 

## float & double:

> لنقوم بجعل ال compiler يتعامل مع الارقام علي انها float بدل double نقوم بوضع **f** بعد الرقم

```c++
double dob=10;
dob=20.5;
float fl= 10.5f+9.5f;
```

---
## char & ascii:

>char=> carry one letter inside a single quote

#### from char into ASCII
```c++
char a = 'A';
cout<< int(a);
cout<< int('&'); // print the ascii num of &
```

#### from  ASCII into  char 
```c++
cout<< char(81); // Q
```

---

## bool & void:

> bool => اي حاجة فيها true or false

>  لا نستخدم في ال Boolean اﻟـ true, false ﻓﻘﻂ وﻟكن ﻣﻦ اﻟﻤﻤﻜﻦ أن ﻧﻘﻮم ب ﺎﺳﺘﺨﺪام ﻣﻌﺎدﻻت او ﻣﻌﺎدﻟﺔ او عملية ﻣﻌﻴﻨﺔ وينتج ﻣﻨﻬﺎ قيمة

```c++
bool is_open = true;
cout<< is_open +10; // 1+10=11

bool test_one = 10>5
cout<< test_one; //1
bool test_two = 10>100
cout<< test_two; //0

bool num1 = 10;
bool num2 = -24;
bool num3 = 0;

cout<<num1; //1
cout<<num2; //1
cout<<num3; //0
```

> void =>  function  بتعمل دور معين لكن مبترجعش قيمة ومش محتاج تعمل return 0;

```c++
void without_value()
{
   nohing to return
}
```

---

## string:
---

## modifiers & type alias:

> Modifiers => نقدر نتحكم فيه زي ال short , long int 

> فكرته انك بتسهل علي نفسك وتحط اسم بسيط لاسم كبير لو هتستخدمه كذا مرة

   * ليها طريقتين => using identifier =long long int
   typedef long long int identifier   

```c++
using pass = long long int;
typedef long long int pass;
pass mynum =2355488684;

cout<< mynum;
```

---
## type conversion (casting): (convert one type to another)

1. implicit conversion:
    * done automatically by compiler
    
2. explicit conversion:
    * conversion is done by the programmer
    * has another name called **type casting**

> data loss when larger type is converted into a smaller type

` تلات حاجات: 1- لو اديته ارقام من نفس النوع وعملت اي operation ساعتها يطلع الناتجج نفس النوع ومفيش مشكلة`

`2- لو اديته ارقام من نوع مختلف وبينهم operaion ساعتها يبقي فيه مشكلة وال compiler هيستناك تحددل نوع الناتج اللي انت عايزه 

`3- لو فيه مشكلة وانت مدتلوش ال type casting هو مبقاش قدامه غير انه يتصرف لوحده (implicit conversion)``

 TYPE CASTING apply on long long
     >يعني لو بتقسم حاجة لونج علي int ال اجابة تطلع long 
      لازم وانت بتعمل type casting  تركز يمين وشمال المعادلة ولما تعمل ال casting خلي البراكيت حولين ال data type



#### implicit conversion table

| name         | periority |     |     |
| ------------ | --------- | --- | --- |
| bool         | lower     |     |     |
| char         | \|        |     |     |
| short int    | \|        |     |     |
| int          | \|        |     |     |
| unsigned int | \|        |     |     |
| long         | \|        |     |     |
| unsiged long | \|        |     |     |
| long long    | \|        |     |     |
| float        | \|        |     |     |
| double       | \|        |     |     |
| long double  | higher    |     |     |

#### explicit conversion

* (data type)variable
* data type(variable)

```c++
double g=34.5
cout<<10+ (int)g;
cout<<10+ int(g);

```
