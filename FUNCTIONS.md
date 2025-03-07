> Rule :  avoid repetition in reusable functions (التعديل يتم مرة واحدة في ال function مش كل شوية)  

[function with naglaa]([Lectures with Notes - Google Drive](https://drive.google.com/drive/folders/1K8galMPYIpkjcdbKzhtIR-iKCAOVsiZY))
#### Types:
1. *built in functions (standard function) (library)* =>جاهزة علطول للاستخدام
2. programmer (user) defined functions => انا اللي بعملها

---
### defined functions:

##### 1.  *declaration*
     * information for compiler (dont store in memory)
     * parameters between () if exist (you can write the types only) 
     * syntax => return_type func_name (par1 , par2)
##### 2. *definition*
    * implementation of what the function does
    * syntax => return_type func_name (par1 , par2) {
                         //block of code
                  }
     * parameters must contain variable type and name
##### 3. call
     * using the function
     * syntax =|> fun_name (arg1 , arg2); // in void functions
                 var = fun_name (arg1 , arg2); // if the fun                                                 return a value
    * arguments can be (values(literals) / variables / expression
    
    * calling fun can be placed in

---
### how to write:

```c++
int multiply(int a ,int b); //declaration
// return_type  name_function (parameters)
int main(){

int result;
result = multiply(i,j); //calling function with arguments i,j
}      // the value returned by function must be stored in a variable of same ty 

int multiply(int a, int b) //definition
{
 return a*b;
}
```
---
### notes:
1. funcion can return 1 value or void

2. parameters in declaration can be data types (without variable name)(لانها مبتحجزش مكان في الميموري لسه)

3. function body is placed after main fun or instead of declaration before main

4. in body => return value type(لازم تخزن اللي هيخرج ف متغير من نفس النوع) , and formal parameters (type, order & number) should match the function declaration

5.  in definition =>  take care (same parameters type, order, num) to the ones in the declaration // name not important to be the same

6. if return a variable it must be as same type as return type
    *  `double sum (int a, int b, int c){
          double result = a+b+c;
          return result;
          }`  

in calling :  * fn_name (list of arguments);  => when the fun return nothing (void)
   
		  * variable (same type of returned fn) = fn_name (list of arguments) ;

          * arguments (type,order,num) should match the function defination

*  Call can be placed in an expression or a cout statement, ONLY if the function has a return value


>ممكن اعمل call function في ال main تحتوي علي عدد من ال functions جوه بعض


> Arguments can be literals, variables, expressions, or combination
     literals: constant
     expression : arithmatic, or if condition

* the value of argument is assigned into the parameters

> في ال memory  انت بتحجز متغيرات لل main  ومتغيرات  لل parameters of function  في different scopes  اصلا ... وقت ال call  بيحصل copy لقيمة متغير ال main ويحطه ف متغير ال function .... ولكن اي لعب جوه ال function وتحديث المتغيرات دة بيبقي جوه ال function فقط ومبياثرش علي متغيرات ال main اطلاقا (بياثر بس علي المغير اللي هيشيل ال return value of function)
> 
![[Screenshot 2025-02-21 151514.png]]
![[Screenshot 2025-02-21 152203.png]]


* **parameter default value** => writing a value to the parameter in func.    definition
     *   عشان لما اجي اعمل call ومحطش argument ياخد ال default value 
     * لو عندك اكتر من parameter يا تحط default value لكله يا تحط للاخير


* array as parameter => to make it dynamic (easy to be modified)
     * ` void calc(int nums[], int count)`
    * وقت ال calling بكتب اسم ال array \ var فقط من غير اقواس 


* in void function => type  (return;) if you want to skip the statements below it
* any statement below the return statement is unseen 
* لو عندك function بترجع قيمة وبتعملها call هتنفذ كل حاجة لحد ال return 
* you can use function in same file or another file in same folder

---

### built-in functions :

1. `#include <cmath>`
     * pow(x,2)
     * sqrt(x)
     * abs(x)
     * fabs(x) =>return absolute for floats/doubles (لا يمكن استخدام ال modulus العادي مع float/double)
     * fmod(10.5, 3) =>return floating point remainder 
     * ceil(x) => round up to nearest int
     * floor(x) => round down to nearest int
     * round(x) => approximate
     * trunc(2.79) => take the int value and remove the points (2)
     * exp(x) => e^x
     * log(x) => log x to the base (e)
     * log10(x) =>log x to the base 10
     * cbrt(x) =>cubic root

2. `#include <cctype>`
     * tolower('A') => make the letter small & give its ascii value  
     * toupper('b') => make the letter capital & give its ascii value(if you want to print the letter so put it in char)
     * isupper , islower  => return bool value (true / false)
     * isspace =>return bool (بيشوف لو عندك اي سبيس او سكيب كاركتر ولو اه يديك ترو)

3. `#include <algorithm>`
     * min(10 , 30 , -40) => least value(argument)
     * min('A' , 'c') => least char according to its ascii value
     * max( {10, 20, 30, 40} ) =>max int 
     // نقدر نحط جواها int, char , array


---

### function overloading:

>using many functions with the same name

##### conditions:  
1. having different num. of parameters
           or
2. having different types of parameters
3. maybe both

> لو عملت نفس اسم ال function بنفس نوع وعدد ال parameters هيطلعلك syntax error


##### example:
```c++
	void print(int a,int b){
cout<<"number one is: "<<a<<"\n";
cout<<"number two is: "<<b<<"\n";
}

	void print(int a, int b, int c){
cout<<"number one is: "<<a<<"\n";
cout<<"number two is: "<<b<<"\n";
cout<<"number three is: "<<c<<"\n";
}

	void print(string a, string b){
cout<<"text one is: "<<a<<"\n"
cout<<"text two is: "<<b<<"\n"
}

	int main(){
print(10,20) // 1st function
print(10,20,30)  // 2nd function
print("OSAMA", "ELZERO");  // 3rd function

return 0;
}
```

---

### function recursion:

> : ﻫﻮ عبارة ﻋﻦ technique ﻣﻦ ﺧﻼﻟﻪ ﻧﺠﻌﻞ اﻟــ function تعمل call لنفسها

```c++
/*
  Function
  - Function Recursion
*/

#include <iostream>
using namespace std;

int add(int num)
{
  if (num == 0)
  {
    return 0;
  }
  cout << num << "\n";
  cout << "===============\n";
  return num + add(num - 1);
}

// 5 + (add(4))
// 5 + ( 4 + add(3) )
// 5 + ( 4 + ( 3 + add(2) ) )
// 5 + ( 4 + ( 3 + ( 2 + add(1) ) ) )
// 5 + ( 4 + ( 3 + ( 2 + ( 1 + add(0) ) ) ) )

int main()
{
  cout << add(5);
  return 0;
}
```