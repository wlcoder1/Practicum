##### Задания для выполнения 
Реализовать протокол Диффи-Хеллмана в виде клиент-серверного приложения. Реализовать клиент-серверную пару, которая шифрует сообщения асимметричным способом Дополнительные задания Модифицируйте код клиента и сервера так, чтобы приватный и публичный ключ хранились в текстовых файлах на диске и, таким образом, переиспользовались между запусками. Проведите рефакторинг кода клиента и сервера так, чтобы все, относящееся к генерации ключей, установлению режима шифрования, шифрованию исходящих и дешифрованию входящих сообщений было отделено от основного алгоритма обмена сообщениями. Реализуйте на сервере проверку входящих сертификатов. На сервере должен храниться список разрешенных ключей. Когда клиент посылает на сервер свой публичный ключ, сервер ищет его среди разрешенных и, если такого не находит, разрывает соединение. Проверьте правильность работы не нескольких разных клиентах. Модифицируйте код клиента и сервера таким образом, чтобы установление режима шифрования происходило при подключении на один порт, а основное общение - на другом порту. Номер порта можно передавать как первое зашифрованное сообщение. Модифицируйте код FTP-сервера таким образом, чтобы он поддерживал шифрование.
#### При запуске сервера мы получаем обратный ответ и видим, какой порт слушается
![image](https://user-images.githubusercontent.com/76069143/146632330-7dd9c71a-2288-4af4-bb42-527f44597b04.png)
#### Напишем обратное сообщение на сервер 
![image](https://user-images.githubusercontent.com/76069143/146632371-57fe8961-7310-4d90-93a3-08e2c2b3d9db.png)
#### После отправки сообщения от пользователя, у нас эти данные отображаются на сервере
![image](https://user-images.githubusercontent.com/76069143/146632566-04d63c4b-be46-46a4-8577-7fad53baba27.png)
#### У нас есть файлы, где хранятся публичные и приватные ключи и переиспользуются между запусками
![image](https://user-images.githubusercontent.com/76069143/146632554-0b33f5f5-ab95-440f-8e0d-4d6983d68a1c.png)
#### Также на сервере хранятся данные по всем возможным ключам, когда клиент посылает на сервер свой публичный ключ, сервер ищет его среди разрешенных и, если такого не находит, разрывает соединение (Данные находятся в файле key_list)
![image](https://user-images.githubusercontent.com/76069143/146632653-036b7753-036a-45b3-85f3-ea77c7b30dda.png)
#### Условие, что может быть несколько клиентов
![imgonline-com-ua-2to1-Puy0fPYs92p1wcne](https://user-images.githubusercontent.com/76069143/146633457-4921557d-d31b-476c-ad00-b67120eb4ee4.jpg)
#### Установление режима шифрования происходило при подключении на один порт, а основное общение - на другом порту. Номер порта можно передавать как первое зашифрованное сообщение. 
![image](https://user-images.githubusercontent.com/76069143/146632968-1ab78d81-fe8e-4e4b-afd2-f03fd1626963.png)
![image](https://user-images.githubusercontent.com/76069143/146632974-9f5d42ce-dc2a-497c-88bd-6ae469bcfce2.png)
