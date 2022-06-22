# React_Middleware

## что такое midlleware  какие бывают    


**midlleware - промежуточное програмное обеспечение которое срабатывает после диспатча и перед редьюсером. midlleware    обрабатывает асинхронную логику
и возвращает результат в редьюсер.**


Посредники (англ. middleware) предоставляют удобный механизм для фильтрации HTTP-запросов вашего приложения  
Middleware — связующее программное обеспечение, которое помогает приложению и серверу обмениваться друг с другом запросами.

https://www.itweek.ru/idea/article/detail.php?ID=51098  
https://www.4stud.info/networking/lecture6.html  
https://surf.ru/chto-takoe-middleware/  

##  отличие thunk  от saga  
https://overcoder.net/q/358476/%D0%B2-%D1%87%D0%B5%D0%BC-%D1%80%D0%B0%D0%B7%D0%BD%D0%B8%D1%86%D0%B0-%D0%BC%D0%B5%D0%B6%D0%B4%D1%83-redux-thunk-%D0%B8-redux-saga#:~:text=%D0%9A%D0%B0%D0%BA%20Redux%20Thunk%2C%20%D1%82%D0%B0%D0%BA%20%D0%B8,%D0%BE%20%D0%B1%D0%BE%D1%80%D1%8C%D0%B1%D0%B5%20%D1%81%20%D0%BF%D0%BE%D0%B1%D0%BE%D1%87%D0%BD%D1%8B%D0%BC%D0%B8%20%D1%8D%D1%84%D1%84%D0%B5%D0%BA%D1%82%D0%B0%D0%BC%D0%B8.&text=%D0%A1%D0%B0%D0%B3%D0%B0%20%D0%B4%D0%B5%D0%BB%D0%B0%D0%B5%D1%82%20%D1%82%D1%80%D0%B8%D0%B2%D0%B8%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%BC%20%D0%BE%D1%82%D0%BC%D0%B5%D0%BD%D1%83%20%D1%8D%D1%84%D1%84%D0%B5%D0%BA%D1%82%D0%B0,%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D1%82%20(%D1%82%D0%B0%D0%B2%D1%82%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8)%20%D0%BE%D1%82%20%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0.   

https://medium.com/@shoshanarosenfield/redux-thunk-vs-redux-saga-93fe82878b2d

https://qna.habr.com/q/407081  


**thunks** - это шаблон написания функций с логикой внутри, которые могут взаимодействовать с методами **dispatch** и **getState** хранилища Redux.  
https://www.youtube.com/watch?v=CtrWoX_KDjE

**Middleware** - https://www.youtube.com/watch?v=ax1verdkVPo

Redux-Thunk, который использует функции обратного вызова, поток Redux-Saga можно запускать, приостанавливать и отменять из основного приложения с помощью обычных действий Redux. 

**Redux-thunk** -  это  middleware for Redux.  
Redux Thunk используется для асинхронного взаимодействия с внешним API с целью получения или сохранения данных.  
Redux Thunk - это Middleware который позволяет внутри сторонних функций исп dispatch

 https://github.com/reduxjs/redux-thunk    
 https://redux.js.org/usage/writing-logic-thunks
 https://www.digitalocean.com/community/tutorials/redux-redux-thunk-ru

Преимущество Redux-Saga по сравнению с Redux-Thunk заключается в том, что вы можете избежать ада обратного вызова  
Кроме того, вы можете более легко протестировать свой асинхронный поток данных.  
Redux-Thunk возвращает обещания, которые сложнее проверить.   
Redux-Thunk, однако, отлично подходит для небольших случаев использования  

https://medium.com/@shoshanarosenfield/redux-thunk-vs-redux-saga-93fe82878b2d

сага позволяет контролировать поток запроса за счёт своих методов +  сагах проще делать интеграционные тесты  
redux-thunk  у него нету понятия как поток не контролирует поток запроса

Redux-thunk vs Redux-saga  
https://medium.com/@shoshanarosenfield/redux-thunk-vs-redux-saga-93fe82878b2d

https://russianblogs.com/article/7913978121/






