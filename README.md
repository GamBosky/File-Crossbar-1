<img align="right" width="150" height="150" src="documentation/fc_icon.jpg">

# TricityTravel

## 1. Specyfikacja wymagań
### 1.1. Opis systemu
#### 1.1.1. Nazwa
Nazwa ogólna: FileCrossbar - instant upload service 
Nazwa krótka: FileCross

#### 1.1.2. Uczestnicy
1. Sebastian Wrzalek
2. Piotr Gambowski
3. Mateusz Arendarski

#### 1.1.3. Charakterystyka
Aplikacja mobilna ułatwiająca podejmowanie decyzji o poruszaniu się po Trójmieście. Uwzględnia wskazówki do podróży komunikacją miejską, poruszania się autem oraz wskazuje aktualną pogodę.

###  1.2. Specyfikacja właściwa - historyjki użytkowników

#### 1.2.1 Wymagania Funkcjonalne
**W1.** Osoba zainteresowana TricityTravel [kto] w ramach dedykowanej platformy sprzedażowej po uprzednim zalogowaniu się na koncie Google [gdzie] może pobrać aplikację na swoje urządzenie mobilne z systemem Android w wersji minimum 6.0 [co]

**W2.** Użytkownik aplikacji TricityTravel [kto] w zakładce z ustawieniami [gdzie] może spersonalizować swoje ustawienia dotyczące poruszania się po Trójmieście (ustawienia pogody; przystanków, z których korzysta użytkownik; wybranej trasy w podróży samochodem; ustawienia tagów do poboru informacji z Trójmiasto.pl) [co].

**W3.** Użytkownik aplikacji TricityTravel [kto] w zakładce "Samochód" [gdzie] wyświetla czas najkrótszego przejazdu od podanego punktu A do B na podstawie danych Here Maps [co].

**W4.** Użytkownik aplikacji TricityTravel [kto] w zakładce "Transport publiczny" [gdzie] wyświetla listę linii transportu publicznego w połączeniu z przystankami, które zostały wybrane w ustawieniach oraz informacje na temat rzeczywistych czasów przyjazdu danego pojazdu na podstawie Otwartych Danych ZTM Gdańsk [co].

**W5.** Użytkownik aplikacji TricityTravel [kto] w zakładce "Pogoda" [gdzie] wyświetla informacje meteorologiczne w wybranym w ustawieniach mieście na podstawie danych OpenWeatherMap [co].

**W6.** Użytkownik aplikacji TricityTravel [kto] w zakładce "Raport" [gdzie] wyświetla informacje z Raportu Trójmiasto (trojmiasto.pl) o utrudnieniach w poruszaniu się po Trójmieście na podstawie tagów (słów kluczowych) wybranych przez użytkownika [co].

![Use cases diagram](/documentation/use_cases_diagram.png)

#### 1.2.2 Wymagania Niefunkcjonalne

**W7.** Użytkownik aplikacji TricityTravel [kto] we wszystkich zakładkach aplikacji [gdzie] sprawnie ładuję dane(do 1s)[co].

## 2. Projekt
### 2.1. Możliwość instalacji i przekazania projektu
Prowadzący ma prawo przekazywać projekt innym studentom w celu dzielenia się wiedzą.

### 2.2. Diagram czynności UML
![Use cases diagram](/documentation/activity_diagram.png)

### 2.3. Diagram komponentów i wdrożenia
![Use cases diagram](/documentation/components_diagram.png)


## 3. Scenariusze testów - testy akceptacyjne
### 3.1. T1 - Instalacja aplikacji
**Scenariusz dotyczy:** W1  
**Cel testu:** Testowanie poprawnego pobierania oraz instalowania aplikacji TricictyTravel na urządzeniu mobilnym.  
**Sposób dostępu:** Widok wywoływany.  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Wyszukanie aplikacji TricityTravel w sklepie Google Play i klinkięcie przycisku pobierz.

#### Odpowiedź systemu:  
1. Urządzenie mobilne pobierze aplikacje.
2. Urządzenie mobilne poinformuję nas o zainstalowaniu aplikacji.

### 3.2. T2 - Personalizacja ustawień - pogoda
**Scenariusz dotyczy:** W2  
**Cel testu:** Testowanie personalizacji ustawień dotyczących pogody.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z menu "Ustawienia"  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Wpisanie w pole tekstowe nazwy miasta.
2. Wybranie przycisku "Zapisz".
#### Odpowiedź systemu:  
1. Poprawne wyświetlenie pogdoy dla wybranego miasta w zakładce "Pogoda".

### 3.3. T3 - Personalizacja ustawień - transport publiczny
**Scenariusz dotyczy:** W2  
**Cel testu:** Testowanie personalizacji ustawień dotyczących transportu publicznego.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z menu "Ustawienia"  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Wybranie przycisku "Edytuj listę linii".
2. Wybranie przycisku "Dodaj" obok wybranego przystanku.
3. Zaznaczenie checkboxem linii, które chcemy dodać do swoich ustawień.
4. Wybranie przycisku "Zapisz".
#### Odpowiedź systemu:  
1. Wyświetlenie listy przystanków.
2. Dodanie przystanku do listy.

### 3.4. T4 - Personalizacja ustawień - tagi
**Scenariusz dotyczy:** W2  
**Cel testu:**  Testowanie ustawienia tagów do poboru informacji z Trojmiasto.pl
**Sposób dostępu:** Widok wywoływany poprzez wybranie z menu "Ustawienia".  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Wpisanie tagu w pole tekstowe.
2. Naciśnięcie enter na klawiaturze ekranowej.
#### Odpowiedź systemu:  
Tag wyświetla się poniżej pola tekstowego.

### 3.5. T5 - Wyświetlenie czasu dojazdu do punktu docelowego
**Scenariusz dotyczy:** W3  
**Cel testu:** Testowanie wyświetlania czasu dojazdu do punktu docelowego dla podanych danych.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z dolnego menu zakladki "Samochód"  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Wpisanie punktu początkowego w pole tekstowe.
2. Wpisanie punktu docelowego w pole tekstowe.
3. Wybranie przycisku "Czas przejazdu"
#### Odpowiedź systemu:  
1. Wyświetlenie informacji na temat czasu dojazdu.

### 3.6. T6 - Usunięcie przystanku z listy
**Scenariusz dotyczy:** W4  
**Cel testu:** Testowanie funkcjonalności usuwania przystanków z listy zapisanych w ustawieniach.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z dolnego menu zakladki "Transport publiczny".  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Naciśnięcie i przytrzymanie na wybranym przystaku.  
2. Wybranie opcji Tak w celu usunięcia przystanku z listy.
#### Odpowiedź systemu:  
1. Aplikacjia usunie przystanek z listy.  

### 3.7. T7 - Negacja usunięcia przystanku z listy
**Scenariusz dotyczy:** W4  
**Cel testu:** Testowanie funkcjonalności usuwania przystanków z listy zapisanych w ustawieniach.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z dolnego menu zakladki "Transport publiczny".  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Naciśnięcie i przytrzymanie na wybranym przystaku.  
2. Wybranie opcji Nie w celu usunięcia przystanku z listy.
#### Odpowiedź systemu:  
1. Aplikacjia nie usunie przystanku z listy.  


### 3.8. T8 - Wyświetlenie rzeczywistych czasów przyjazdu
**Scenariusz dotyczy:** W4  
**Cel testu:** Testowanie funkcjonalności wyświetlenia rzeczywistych czasów przyjazdu danego pojazdu.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z dolnego menu zakladki "Transport publiczny".  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Kliknięcie na wybrany przystanek.  
2. Przeciągnięcie palcem w dół - odświeżenie widoku.
#### Odpowiedź systemu:  
1. Odświeżenie listy linii.
2. Wyświetlenie rzeczywistych czasów przyjazdów(opóźnienie - kolor czerwony, punktualny - kolor zielony, przed czasem - kolor pomarańczowy).

### 3.9. T9 - Wyświetlenie informacji pogodowych
**Scenariusz dotyczy:** W5  
**Cel testu:** Testowanie funkcjonalności wyświetlenia informacji pogodowych.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z dolnego menu zakladki "Pogoda".  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Kliknięcie przycisku "Odśwież" - odświeżenie danych.
#### Odpowiedź systemu:  
1. Wyświetlenie aktualnych danych pogodowych.

### 3.10. T10 - Wyświetlenie raportu Trójmiasto
**Scenariusz dotyczy:** W6  
**Cel testu:** Testowanie funkcjonalności wyświetlenia Raportu Trójmiasto.  
**Sposób dostępu:** Widok wywoływany poprzez wybranie z dolnego menu zakladki "Raport".  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Brak.
#### Odpowiedź systemu:  
1. Wyświetlenie listy nagłówków z Raportu Trójmiasto.

### 3.11. T11 - Pomiar szykbości aplikacji
**Scenariusz dotyczy:** W7  
**Cel testu:** Testowanie szybkości aplikacji.   
**Sposób dostępu:** Widoki wywoływane przez wybranie z dolnego menu kolejnych zakładek.  
**Scenariusz (kroki testowe):**   
#### Akcje użytkownika:  
1. Wybranie zakładki "Pogoda".
1. Wybranie zakładki "Transport publiczny".
1. Wybranie zakładki "Samochód".
1. Wybranie zakładki "Raport".
#### Odpowiedź systemu:  
1. Subiektywnie szybkie (do 1s) wyświetlenie widoku.

## 4. Instrukcja instalacji i uruchomienia
### 4.1 Instalacja aplikacji na urządzeniu mobilnym w celu testowym
1. Skopiowanie pliku .apk z folderu /apk projektu na urządzenie mobilne z systemem Android w wersji 6.0 lub wyższej,
2. Wyszukanie pliku na urządzaniu mobilnym i instalacja aplikacji,
3. (Opcjonalnie) Zezwolenie na instalację aplikacji z nieznanych źródeł.

### 4.2 Uruchomienie projektu w celu dalszego rozwoju
1. Pobranie i instalacja programu Android Studio w wersji 3.4 lub wyższej,
2. Rozpaknowanie pliku .zip, lub sklonowanie projektu z serwisu GitHub do dowolnej lokalizacji na komputerze,
3. W Android Studio wybranie opcji File/Open i wskazanie rozpakowanego projektu. Android Studio automatycznie pobierze wszystkie wymagane biblioteki i skompiluje projekt,
4. Utworzenie bezpłatnych kont w serwisach https://openweathermap.org/ oraz https://developer.here.com/ i wygenerowanie kluczy API,
5. W folderze \app\src\main\java\com\aib\tricitytravel\data utworzenie pliku APIKeys.kt o zawartości podanej poniżej oraz zamiana odpowiednich pól na własne, wygenerowane wcześniej, klucze API,
```kotlin
package com.aib.tricitytravel.data

object APIKeys {

    const val OPEN_WEATHER_KEY = "<tu wkleić klucz OpenWeatherMap>"
    const val HERE_APP_ID = "<tu wkleić klucz Here App ID>"
    const val HERE_APP_CODE = "<tu wkleić klucz Here App Code>"
}
```
6. Utworzenie bezpłatnego konta w serwisie https://firebase.google.com/,
7. Utworzenie projektu o dowolnej nazwie w serwisie Firebase i postępowanie zgodnie z instrukcjami w celu podłączenia projektu w Android Studio z projektem w Firebase,
8. Wdrożenie cloud function z folderu /firebase_cloud_functions w utworzonym projekcie Firebase zgodnie z instrukcją na stronie https://cloud.google.com/functions/docs/deploying/filesystem,
9. Podmiana odnośnika "FIREBASE_DOMAIN" w pliku /data/URLs.kt na własny znajdujący się w zakładce "Functions" w serwisie Firebase,
```kotlin
package com.aib.tricitytravel.data

object URLs {
    const val ZTM_DOMAIN = "http://87.98.237.99:88/"
    const val FIREBASE_DOMAIN = "<tu wkleić własny link do cloud function downloadBusStopsFromFirebase>"
    const val OPEN_WEATHER_DOMAIN = "https://api.openweathermap.org/"
    const val HERE_GEOCODER_DOMAIN = "https://geocoder.api.here.com/"
    const val HERE_ROUTE_DOMAIN = "https://route.api.here.com/"
    const val TROJMIASTO_REPORT = "https://www.trojmiasto.pl/raport/"
}
```
10. W Android Studio kliknięcie Run/Run 'app' i wybranie emulatora lub fizycznego urządzenia w celu uruchomienia aplikacji.

## 5. Uwagi ogólne

### 5.1 Skrótowy opis głównych pakietów
 - data - zawiera klasy odpowiedzialne za pobieranie danych z web service'ów, zapis w lokalnej bazie danych, a także wszystkie modele i obiekty DTO (Data Transfer Objects),
 - di - zawiera moduły i komponenty wykorzystywane przez bibliotekę Dagger 2 potrzebne do wstrzykiwania zależności (Dependency Injection),
 - ui - zawiera wszystkie klasy widoków w aplikacji, wewnątrz pakietu zastosowany jest dodatkowy podział według zasady "package by feature",
 - util - zawiera klasy pomocnicze m. in. wykorzystywane w data binding.

### 5.2 Licencja
```
Copyright © 2019 by Agnieszka Maciejewska, Maciej Królik, Krzysztof Mikołajczyk. TricityTravel
This application is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License.
To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-nd/4.0/.
```