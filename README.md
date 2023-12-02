# Odkaz na server
http://16.171.11.82/


# Popis Aplikace
Tato aplikace slouží k správě informací o knihách. Umožňuje uživatelům získat seznam všech knih, přidávat nové knihy, aktualizovat informace o existujících knihách a odstraňovat knihy ze systému.

# Endpointy

Metoda: GET
Endpoint: /
* Autentizace: Ano (kontrola pomocí checkAuthenticated middleware)
* Popis: Vrátí seznam všech knih uložených v systému.
* Odpověď při úspěchu (HTTP kód 200): Seznam knih ve formátu JSON.
* Odpověď při chybě (HTTP kód 404): Chybová zpráva v případě problému s dotazem na databázi.

Metoda: POST
Endpoint: /
* Autentizace: Ano (kontrola pomocí checkAuthenticated middleware)
* Popis: Přidá novou knihu do systému na základě poskytnutých informací.
* Odpověď při úspěchu (HTTP kód 200): Potvrzující zpráva o úspěšném přidání knihy.
* Odpověď při chybě (HTTP kód 404): Chybová zpráva v případě nesprávně poskytnutých informací nebo problému s databází.

Metoda: PUT
Endpoint: /
* Autentizace: Ano (kontrola pomocí checkAuthenticated middleware)
* Popis: Aktualizuje informace o existující knize na základě poskytnutých informací.
* Odpověď při úspěchu (HTTP kód 200): Potvrzující zpráva o úspěšné aktualizaci knihy.
* Odpověď při chybě (HTTP kód 404): Chybová zpráva v případě nesprávně poskytnutých informací nebo problému s databází.

Metoda: DELETE
Endpoint: /
* Autentizace: Ano (kontrola pomocí checkAuthenticated middleware)
* Popis: Odstraní knihu ze systému na základě poskytnutého identifikátoru knihy.
* Odpověď při úspěchu (HTTP kód 200): Potvrzující zpráva o úspěšném odstranění knihy.
* Odpověď při chybě (HTTP kód 404): Chybová zpráva v případě nesprávně poskytnutého identifikátoru knihy nebo problému s databází.
