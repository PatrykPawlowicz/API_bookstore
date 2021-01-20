# API Biblioteka

## Krótki opis
API biblioteki umożliwiające:
<ul> 
  <li> pobieranie danych książek,
  <li> modyfikowanie danych książek,
  <li> dodawanie nowych pozycji,
  <li> usuwanie niepotrzebnych pozycji z bazy danych
</ul>

## Pobieranie danych
Do pobrania danych należy:
<ol>
  <li> Utworzyć konto użytkownika, ścieżka: (user/register), podając imię, mail oraz hasło w pliku JSON, 
  <li> Zalogować się, ścieżka: (user/login)
  <li> Pobrać token uwierzytelnijący (unikalny dla każdego profilu) aby uzyskać dostęp do bazy książek, ścieżka: (/books).
</ol>

W celu uruchomienia należy utworzyć plik .env oraz podać string DB_CONNECT w celu połączenia z bazą danych.

## Technologia

Logowanie użytkowników jest walidowane pod kątem odpowiednich parametrów podawanych podczas tworzenia konta, jak i przy logowaniu. Hasło przechowywane w bazie danych jest zaszyfrowane. Token uwierzytelniający jest generowany dla nowego użytkownika, bez niego nie uzyskamy dostępu do bazy danych z książkami.

Wersje frameworków:

    "@hapi/joi": "^15.0.3",
    "bcryptjs": "^2.4.3",
    "body-parser": "^1.19.0",
    "dotenv": "^8.2.0",
    "express": "^4.17.1",
    "jsonwebtoken": "^8.5.1",
    "mongoose": "^5.11.12",
    "morgan": "^1.10.0", 
    "nodemon": "^2.0.6" 
    
## Przykłady działania
 ![Rejestracja](./screenshoots/Zrzut ekranu (7).png)
 <br>
 ![Rejestracja](./screenshoots/Zrzut ekranu (8).png)
 <br>
 ![Rejestracja](./screenshoots/Zrzut ekranu (9).png)
 <br>
 ![Logowanie]()
 <br>
 ![Lista książek](./screenshoots/Zrzut ekranu (11).png)
 <br>
 ![Dodawanie książki](./screenshoots/Zrzut ekranu (13).png)
 <br>
 ![Zaktualizowana lista książek](./screenshoots/Zrzut ekranu (14).png)
 <br>
 ![Wyszukiwanie ksiązki po ID](./screenshoots/Zrzut ekranu (12).png)
 <br>
