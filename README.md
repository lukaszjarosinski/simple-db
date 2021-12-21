# MySQL queries
Prosta klasa PHP, umo�liwiaj�ca podstawow� obs�ug� baz danych MySQL z u�yciem rozszerzenia PDO. Obs�uguje najcz�ciej wykorzystywane w codziennej pracy rodzaje zapyta�.
## Dzia�anie
Na pocz�tek ��czymy si� z baz� danych
```php
		$db = new Base;
		$db->connect($db_user,$db_password,$db_host,$db_name);
```
Spos�b wykonania zapyta� do bazy
```php
		a. $db->query("INSERT INTO `tabela` VALUES(NULL,'wartosc','wartosc')");
		b. $db->query("DELETE FROM `tabela` WHERE `id` = '1'");
		c. $db->query("SELECT * FROM `tabela` WHERE `id` = '1'");
		d. $db->query("UPDATE `tabela` SET `username` = 'nazwa_uzytkownika' WHERE `id` = '1'");
```
Dla zapytania a zwracane jest ID ostatniego wstawionego rekordu.
Dla zapyta� b i d zwracana jest liczba zmodyfikowanych/usuni�tych rekord�w.
Dla zapytania c zwracana jest tablica asocjacyjna zawieraj�ca rekordy odpowiadaj�ce zapytaniu.