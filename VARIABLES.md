[C++ Variables](https://www.w3schools.com/cpp/cpp_variables.asp)

* #### declaration & initialization
* #### naming rules
 * #### scopes
 * #### constant variable
 * #### escape sequence
---

## naming rules:
 1. Must Be Unique 
 2. Case Sensitive (capital & small)
 3. Cannot Start With Numbers 
 4. Numbs Or Letters Or Underscore (Accepted)
 5. No Space Or Special Characters (اللي بعد الباكسلاش)
 6. Reserverd Keywords (لا يمكن استخدام الكلمات المحجوزة اوردي في اللغلة)
 ---
## scopes:
1. global
    * can be **used** by any function
    *  **aren't declared** in any function
    * any declared variables has value = 0

2. local
    * declared inside a function
    * cant be used outside the curley praces of its scope

---
## constant variable:
* Read Only Value  
* Can't be Declared Without Value
* ` const int num= 100;`

---
## escape sequence:
 *  \n => new line
 *  ` \\`=> print  \
 *  `\"` => print "
 * `\'` => print '
 *  \t => Tab Equal 8 Spaces 
 * \b => backspace
 * \a => Alert => Play Beep During Execution 
 * \r => Carriage Return

---
### notes on local var:
* can have the same names in different scopes (same name but totally different in memory location)
* also we can use same name in different functions

### notes on global var:
* global function is declared to all functions below it
* ال local اقرب للقلب من ال global يعني لو عندك متغيرين واحد جلوبال وواحد لوكال ف fn معينة ال function هتعتبرك بتتكلم عن ال local لكن لو دخلت fun تانيه هتتعامل بالجلوبال عادي