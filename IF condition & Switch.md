
[C++ If ... Else](https://www.w3schools.com/cpp/cpp_conditions.asp)


1. لو عندك كذا if بيقراهم كلهم ولكن لو if_else هيقرا لحد ما الشرط يكون صح ويكنسل الباقي
2. ممكن متفحش curley praces لو هتكتب سطر واحد بس جوه

# ternary operator

     cout<<(condition) ? action when true : action when false ;
```c++
int time = 20;  
string result = (time < 18) ? "Good day." : "Good evening.";  
cout << result;
```
3. Nested ternary operator
     cout<<(age>=17 ? "ok age" :(points>1000? "ok p":"no sorry"));
     
___
# switch case
``` CPP
switch(day) //variable which cases depends on
case 1:
  cout<<"First day";
  break;
case 2:
  cout<<"second day";
  break; 
  /* 1. break is optional but in this example its important..if we remove break from any case it will continue to the second.

    2. if there is more than one case are similar w can confuse them like that : ( case 1:
                   case 2:
                     cout<<"similar cases"; )

```

> 1. لو مستخدمتش break هيخش في اللي تحتيه
> 2. ال switch لا يقبل بنوع بيانات غير int , char
> 3. لو فيه اكتر من case  ليهم نفس ال output تقدر تدمجهم سوا 


* في ال IF statment لو اللي جواها true او bool قيمته true هينفذ اللي جواها




