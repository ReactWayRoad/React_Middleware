##  Redux-Saga  

https://www.youtube.com/watch?v=ylhHYtTyVGE

**Redux-saga** is a library that aims to make application side effects  
(i.e. asynchronous things like data fetching and impure things like accessing the browser cache)
easier to manage, more efficient to execute, easy to test, and better at handling failures. 

Redux-saga -  это middleware для  redux цель которого сделать  асинхроные операции эффективными для выоплнения, легкоуправляемыми и тестируемыми    
**Цель саги**  создать отдельный поток который  отвечает  за все асинхронные действия в приложении (доступ в кеш, запросы ...)  
**Redux-saga** построена на es6 генераторах что позволяет уддобно  писать и тестировать асинхронный код 

**Redux-saga** is a redux middleware.  

### Effect  

An effect is a plain JavaScript Object containing some instructions to be executed by the saga middleware.  

**call**  
return data from Promise  

**all**  
combine two or more watchers

**take**  
Creates an Effect description that instructs the middleware to wait for a specified action on the Store.  
The result of yield take(pattern) is an action object being dispatched.

### Watcher/Worker

**The watcher: will watch for dispatched actions and fork a worker on every action**  
**The worker: will handle the action and terminate**  

В этой библиотеке есть  **workers watchers effects**

**worker**(бизнес логика) - это функция внутри которой выполняется какае-то асинхронная лога (timeout, запросы на сервер...)  
**watcher** - это функция генератор в которой мы с помощью специальных функций указываем тип action и worker, которые будет отрабатывать, когда action  с таким  
типом, который мы указали будет отрабатывать  
**watcher**( следит  за эффектами) это функция наблюдатель, которая ждёт пока отработает тот или иной action, если к этому action  привязан какой-то **worker**(простая асинхронная  функция, то **watcher** эту функцию вызывает.  
**effects** -  набор встроенных в redux saga  функций, которые помогают делать запросы, делать  dispatch, следить за **workers** и т д 

Saga построена вокруг генераторав - это функция  помеченная * и которая возвращает данные поэтапна. yield.  
**функции генераторы** помечены * и вних  исп ключ  слово yeld( может возвращать промежуточный результат, приостанавливать вып функ, в любой момент возвращаться  
и продолжать её выполнение)    
чтобы получить значение из генератора надо вызвать у генератора метод  next()

![Screenshot_19](https://user-images.githubusercontent.com/66359081/160393458-0af361ac-bf0c-42a0-b9ac-cff502f04c3e.png)

### Blocking/Non-blocking call  

**A Blocking call** means that the Saga yielded an Effect and will wait for the outcome of  
its execution before resuming to the next instruction inside the yielding Generator.

**A Non-blocking** call means that the Saga will resume immediately after yielding the Effect.


