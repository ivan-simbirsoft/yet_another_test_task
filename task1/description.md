# TASK1

##Задание
> Задание: Спроектировать схему БД для хранения библиотеки. Интересуют авторы и книги.
> 
> Дополнительное задание: Написать SQL, который вернет список книг, написанный ровно 3 соавторами. Результат: книга - количество соавторов.
> Решение должно быть представлено в виде ссылки на https://www.db-fiddle.com/.

##Решение

При проектировании структуры БД будем придерживаться предметно-ориентированного подхода.
Предметная область содержит два типа сущностей - "книга" и "автор", 
в БД они будут храниться в таблицах `book` и `author` соответственно. 

Условия предметной области - у "книги" может быть несколько "авторов", 
у "автора" может быть несколько "книг". Эту зависимость "многие-ко-многим" 
в реляционной СУБД можно реализовать с помощью дополнительной таблицы связи "book_author".

Скрипт создания таблиц, наполнения их данными и требуемая выборка находится по [ссылке](https://www.db-fiddle.com/f/5azp2FRNGs2h3FUQrRoNHL/2)