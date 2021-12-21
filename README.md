# MySQL queries
Prosta klasa PHP, umo¿liwiaj±ca podstawow± obs³ugê baz danych MySQL z u¿yciem rozszerzenia PDO. Obs³uguje najczê¶ciej wykorzystywane w codziennej pracy rodzaje zapytañ.
## Dzia³anie
Na pocz±tek ³±czymy siê z baz± danych
```php
		$db = new Base;
		$db->connect($db_user,$db_password,$db_host,$db_name);
```
Sposób wykonania zapytañ do bazy
```php
		a. $db->query("INSERT INTO `tabela` VALUES(NULL,'wartosc','wartosc')");
		b. $db->query("DELETE FROM `tabela` WHERE `id` = '1'");
		c. $db->query("SELECT * FROM `tabela` WHERE `id` = '1'");
		d. $db->query("UPDATE `tabela` SET `username` = 'nazwa_uzytkownika' WHERE `id` = '1'");
```
Dla zapytania a zwracane jest ID ostatniego wstawionego rekordu.
Dla zapytañ b i d zwracana jest liczba zmodyfikowanych/usuniêtych rekordów.
Dla zapytania c zwracana jest tablica asocjacyjna zawieraj±ca rekordy odpowiadaj±ce zapytaniu.