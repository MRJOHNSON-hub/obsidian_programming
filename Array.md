 >1. What is Array?
 >    An array is a **container** that contains a group of elements of the **same type**, such as integers, characters,... etc.

>Placed in Contiguous Memory (يحجز اماكن جمب بعض في الميموري)
>كل عنصر من العناصر ليه index خاص بيه يبدا ب 0 ويبتهي عند no.elements-1

---
#### syntax:

`data type  name [no.elemnt] = {e1, e2, ....}`
```c++
int nums[4] = {100, 200, 300, 400};
int nums[4]{100, 200, 300, 400};
int nums[]{100, 200, 300, 400};
```
 declaring multiple arrays of same type:
 `int nums[3],data[5];`
 ---

#### Access:

* **size of array (how many bytes in memory)**
* **elements** =>array & index
* **memory location**

```c++
int nums[]{100, 200, 300, 400,};

cout<<sizeof(nums); // 4*4= 16 bytes

cout<<nums[0]; //1st element
cout<<nums[1]; //2nd element
cout<<nums[2]; //3rd element
cout<<nums[3]; //last element
// array[index]

cout<< &nums[0];
```

---

#### how to deal:

*  *declare empty array*
*  add elements to array

>array only declared once (no. of elements cant be changed)


```c++
int nums[4]; // empty array (no. of elements is 4)

nums[3]= 400; //initialize the last element (هنا بتكلم علي ال index =3)
nums[2]=300;// third elemet
nums[0]=100; //1st element

cout<< sizeof(nums)/sizeof(nums[0]);// 16/4
// no. of elements
cout<< size(nums);
```

---

#### 2D_Array:

rows => no. of arrays
columns => no. of elements in 1 array

`2D Array => int nums[rows][columns] = {{1, 2, 3}, {4, 5, 6}}`

```c++
int points[3][4] ={{1, 2, 3, 4 }, {5, 6, 7, 8}, {9, 10, 11, 12}
};

cout<<points[1][2]; //7   الارقام دي index
cout<<points[2][0]; //9   الارقام دي index
```

> لا يمكن تعريف array  بمتغير الا اذا كان const var.

```c++
const int rows=3;
const int columns =4;

int points[rows][columns] = {         };
```

> تقدر تاخد input من ال user وتخليه index لل array بتاعك

```c++
	int i;
	cin>>i;
	int nums[i];
```
---
#### types of array:
1.  *C-style:*
     * int points [] ={1, 2, 3, 4};
     >فيها شوية مشاكل
     
1.  *vector(class array)*:
     * `#include <array>`
     * template <type , size> identifier;


```
#include <array>

array<int,4> points ={1, 2, 3, 4};

cout<< points[1]; // 2;
```
---
#### Array method discussion:

>**in vector array only**

  * size() =>> display  no of elements
  * fill() =>> make all index with the same value
  * front() => > display  value of index 0
  * back() => > display  value of the last element
  * at() => >display value based on its index
  * empty() =>> check if the array is empty or not


```c++
array<int,4> nums ={100, 200, 300, 400};

cout<< nums.size()
 nums.fill() // if fill by a char then will print the ascii value
// if filled by boolean(true/false) print 1 for true & 0 for false
cout<< nums.front()
cout<< nums.back()
cout<< nums.at(1) //print the no. at index 1

cout<< nums.empty() // (booleN VALUE) print 1 if it is empty & print 0 if it is not empty array
```

---
#### Additional notes:

1.  ```
int array[4] = {5, 8};
The array will contain the values 5, 8, 0 and 0

* in declaration => `int arr[5] = int arr[3+2] = int arr[const size +3] where size is const var = 2`

* array size must be const but ... index can be variable
* index out of bound ! => garbage value (لو حطيت رقم اندكس اكبر من اللي متاح هيجيبلك اي ارقام)

* When an array is created, its elements are assigned with
arbitrary values (Garbage) (unknown values)

* during initializing elements of array :  
   1. if not enough => the rest element values will be zeroes 
   2. if too many => syntax error

> `int bar[5];  //garbage values
> `int bar[5] = {};  //all elements are 0

* you cant copy all array elements to another array one time(you can use for loop and copy each index)
     ```c++
     arr1[5]= arr2[5]; //wrong
     for(int i=0; i<5; i++)
     arr1[i]=arr2[i]; //right
```

* rand () %100 =>generates random numbers from 0 to 99

---

#### string (char array):

1. *C- style  array*
2. *class array (vector)*


##### C style:

```c++
char name_a[9]= {'H', 'e', 'l', 'l', 'o', '1', '2', '3', '@'};
char name_b[10] = "Hello123@";
char name_c[]= {'H', 'e', 'l', 'l', 'o', '1', '2', '3', '@', '\0'};
cout<<name_a; //hello123@ + اي عبط متخزن في الميموري عشان انت محطتش بايدك \0

cout<<name_b; //hello123@  هيقف بعد كدة عشان اوتوماتيك بيحط \0

cout<<sizeof(name_a) // 9
cout<<sizeof(name_c) // 10
cout<<sizeof(name_b) // 10
```

> لو بتكتب بالطريقة الاولي ال size  هيكون نفس عدد الحروف (مش بيزود ال null) الا لو حطيتها انت بايدك
> التانية بيحط تلقائي ال null ( \0 )

*  null character ('\0') indicates the end of characters => any character after it will be neglected`

``` c++
char arr[5] = {'a', 'b', '\0', 'd', 'e'};
cout << arr << endl;
//output will be [ab] only

char name_b[] = "Hello\0123@";
cout<<name_b // hello 
```

##### class array (vector):

```c++
string name = "john"; 

cout<<name  // john
cout<<sizeof(name) // بتختلف من compiler لتاني
cout<<name[0] //j
cout<<name[3] //n
```

>هنا بردو حاطط ال null automatic   ف يعتبر عندك 5 عناصر 


##### concatenating strings:
> ربط ال strings ببعضها

1. normal way
2. strcat =>`#iclude <string.h> ``(#include <cstring>)`
3. +   => `must be string(class/vector)`
4. append => `must be string(class/vector)`

```c++
#include <string.h> //<cstring>
char fname[] = "john";
char lname[] = "ayman";

cout<<fname<< lname; //1st
cout<< strcat(fname,lname); //2nd

string firstname = "osama";
string lastname = "elzero";

cout<< firstname + lastname; //3rd

cout<< firstname.append(lastname); //4th

```

### extra notes:

* `char letters [5] = {'a', 'x'} ` =>the other elements are null
*