
> for (initialization; condition; update)

initialization => ممكن يبقي قبل اللوب اصلا
     `int i=0 ;
     for( ; i<5 ; i++)`

update => ممكن يحصل جوه اللوب اصلا
     `for( ; i<5 ; )
     i++ ;`

condition => ممكن اعمل شرط break جوه اللوب
     `for ( ;  ; ) {
     if (i  == 5)
     break ;
     i++ }`

> while (true) :  هنا اللوب هتفضل مستمرة لد ما تحطلها شرط يوقفها


> **for*** =|> when you have known no. of iteration
> **while** =|> when we have a loop based on a condition
> **Do while** =|> act as while but do first then check the condition