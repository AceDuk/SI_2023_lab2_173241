# Втора лабораториска вежба по Софтверско инженерство

## Александар Дукадиноски, бр. на индекс 173241

###  Control Flow Graph

![Control Flow Graph](cfg.png)

### Цикломатска комплексност

Се пресметува со следниве формули:
V(G) = E – N + 2
V(G) = P + 1
Цикломатската комплексност изнесува 11.

Исто така, со одредување на региони во графот
E = број на врски
N = број на јазли
P = број на предикатни јазли


### Тест случаеви според Multiple condition критериумот

Во оваа класа, условот if (user==null || user.getPassword()==null || user.getEmail()==null) проверува дали корисникот или неговите информации (лозинката и е-поштата) се null. Во споредба со Multiple Condition критериумот, имаме три услови кои треба да ги разгледаме.

##### Тест 1: 
Тест случај кога корисникот (user) е null:

Влезни податоци: user = null, allUsers = [user1, user2, user3]
Очекуван резултат: RuntimeException со порака "Mandatory information missing!"

##### Тест 2: 
Тест случај кога лозинката (password) е null:

Влезни податоци: user = User("username", null, "email@example.com"), allUsers = [user1, user2, user3]
Очекуван резултат: RuntimeException со порака "Mandatory information missing!"

##### Тест 3: 
Тест случај кога е-поштата (email) е null:

Влезни податоци: user = User("username", "password", null), allUsers = [user1, user2, user3]
Очекуван резултат: RuntimeException со порака "Mandatory information missing!"

##### Тест 4: 
Тест случај кога сите информации на корисникот се достапни:

Влезни податоци: user = User("username", "password", "email@example.com"), allUsers = [user1, user2, user3]
Очекуван резултат: Од зависност на други услови во кодот, резултатот може да биде true или false. За овој тест случај, ќе треба да се направат дополнителни тестови за да се проверат и другите услови.
