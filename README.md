# Profiler
Простой профайлер для измерения времени работы отдельных блоков программы или всей целиком 

Как пользоваться:
1. Нужный блок программы взять в фигурные скобки:
  ```
{
        vector <int> simple;
        for (int i = 0; i < 1000; ++i) {
            simple.push_back(i);
        }
}
  ```
  
2. Добавить в начало блока макрос с параметром(сообщением) для идентификации с потоке вывода:
```
{
       LOG_DURATION("time_to_push_back");
       vector <int> simple;
        for (int i = 0; i < 1000; ++i) {
            simple.push_back(i);
        }
}
```
3. Если все сделали правильно то в консоли должен быть такой вывод:
```
time_to_push_back :2394 ms
