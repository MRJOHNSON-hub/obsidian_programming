> is a dynamic array => container for similar data & can control its size
> vector is a class template


### syntax:

`#include <vector>`
   *  `vector <type> variable name`

```c++
#include <vectors>

vector<int> numsOne = {10,20,30,40};
vector<int> numsTWO {10,20,30,40};
vector<int> numsThree (4, 50); // 4 elements of values 50
//هنا الوحيد اللي حدد size 
```

### حاجات معملهاش :

* ` numsThree[4] = 1000;`  //error
     متضيفش عنصر زي ال array بال square bracket


### details:
>تظهر خصائص ال class بعد ال dot

```c++
numsOne.size(); //no. of elemnts
numsOne.at(index) =1000; // initialize or reassiging
cout<<numsOne.at(index); // display the value
numsOne.push_back(55); // add new element to the vector
```




   

