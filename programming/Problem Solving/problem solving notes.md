
# `1. # include <iomanip>

* cout<<fixed<< setprecision(2) <<num ;
//print exactly 2 digits after the decimal point
____

# `2. # include <cmath>
1. sqrt (num) // for square root
2. pow (base , power) //2^3
3. abs (x-y) //absolute

___

# `3. # include <limits .h>

* cout<< INT_MIN;
* cout<< INT_MAX;

---

##### time complexity:

- The amount of computer steps it takes to run an algorithm or code


1 sec ===> 1e8 (`10^8`) 

>compiler can maximum compile `10^8` iteration per second


#### time complexity cases:

* best case
* average case
* worst case


| case                                   | complexity (big O notation) (no. of iterations)             | final O |
| -------------------------------------- | ----------------------------------------------------------- | ------- |
| loop with n iteration                  | n                                                           | O(n)    |
| consecutive loops                      | n + m (add no. of iterations)                               | O(n+m)  |
| nested loop                            | n*m                                                         | O(n*m)  |
| constant                               | 1                                                           | O(1)    |
| consecutive loops with same iterations | n+n =~~2~~n (ignore constants and lower terms.)             | O(n)    |
| nested loop then loop                  | n^2 + ~~n~~ (ignore lower terms only dominant part matters) | O(n^2)  |




---
1. swap(a,b)
//تبديل القيمة المحجوزة في المتغير


2. take care in calculations from the overflow 
    int n,x,y
    cout<<n*(y-x) // this operation could exceed the range of int
    cout<<(long long) n*(y-x) // TYPE CASTING make the result in long long


3. TYPE CASTING apply on long long
     >يعني لو بتقسم حاجة لونج علي int ال اجابة تطلع long 
      لازم وانت بتعمل type casting  تركز يمين وشمال المعادلة ولما تعمل ال casting خلي البراكيت حولين ال data type


4. لمعرفة عدد عناصر الarray تقدر تستخدم size (array_name)
  