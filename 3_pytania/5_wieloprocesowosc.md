# Wieloprocesowość

## Wymień własności określające poprawność programu sekwencyjnego

Wykład "WdWK - wieloprocesowość.pdf" slajd 2

---

- własność stopu (poprawności całkowitej): program na pewno się zatrzyma
- własność częściowej poprawności: jeśli się zatrzyma, zwróci poprawny (zgodny z algorytmem) wynik

## Jakie warunki muszą być spełnione, aby program sekwencyjny był poprawny?

Wykład "WdWK - wieloprocesowość.pdf" slajd 2

---

- wykorzystanie instrukcji, które procesor jest w stanie wykonać
- wszystkie zmienne muszą być jednoznacznie identyfikowalne
- jest dostępna w programie instrukcja zatrzymania procesora

## Zdefiniuj czym jest proces

Wykład "WdWK - wieloprocesowość.pdf" slajd 4

---

Proces (inaczej zadanie) - każdy program w trakcie wykonania. Ponadto program może mieć wiele niezależnych realizacji - osobne procesy.

## Na czym polega współbieżność procesu?

Wykład "WdWK - wieloprocesowość.pdf" slajd 4

---

Współbieżność procesu następuje, gdy jeden proces rozpoczyna się przed zakończeniem drugiego - innymi słowy jednocześnie jeden procesor obsługuje wiele procesów (zadań).

## Wymień warunki poprawności procesu współbieżnego

Wykład "WdWK - wieloprocesowość.pdf" slajd 4, 7

---

- własność żywotności:
  - każde oczekiwane zdarzenie nastąpi
  - każdy proces ma realną szansę wykonania
- własność bezpieczeństwa: program jest zawsze w stanie pożądanym (w pełni kontrolowane są stany wszystkich procesów)

## Wymień typy systemów operacyjnych z perspektywy zarządzania zadaniami i zasobami

Wykład "WdWK - wieloprocesowość.pdf" slajd 5

---

- system wsadowy (serial batch)
- system wieloprogramowy (multiprogramming)
- system z podziałem czasu (time-sharing)

## Wymień funkcje które pełni system operacyjny

Wykład "WdWK - wieloprocesowość.pdf" slajd 6

---

- nadzorowanie procesu (tworzenie środowiska wykonania, aktualizacja struktur danych procesu, synchronizacja i przełączanie procesów, szeregowanie, raportowanie)
- ochrona procesu (przydział i ochrona zasobów, zarządzanie pamięcią, obsługa wyjątków)
- sterowanie i utrzymanie kontroli nad programem
- obsługa wejścia oraz wyjścia
- obsługa plików

## Jakie zasady powinna spełniać ochona zasobów?

Wykład "WdWK - wieloprocesowość.pdf" slajd 8

---

- zapobieganie
- reagowanie na ingerencję w mechanizm ochrony: wykrywanie błędów i ataków, rozpoznawanie i neutralizacja skutków ingerencji, unieważnianie działań ingerujących w mechanizm ochrony

## Na czym polega wspomaganie ochrony zasobów na poziomie architektury rzeczywistej?

Wykład "WdWK - wieloprocesowość.pdf" slajd 8

---

- uniemożliwienie wykonania instrukcji uprzywilejowanych (przestrzeń kodów)
- wykluczenie wykonania w trybie użytkownika operacji używających zastrzeżonych operandów (przestrzeń operandów)
- kontrolowany dostęp do danych (przestrzeń danych)

## Do czego służą furtki (gates) w systemie operacyjnym?

Wykład "WdWK - wieloprocesowość.pdf" slajd 8

---

Zapewniają kontrolowany dostęp do procesów uprzywilejowanych

## Wymień tryby operacji (Modes of operation) w architekturze x86

Wykład "WdWK - wieloprocesowość.pdf" slajd 9

---

- protected mode
- real-adress mode
- system management mode
- virtual 8086 mode

## Wymień kolejne poziomy uprzywilejowania w architekturze x86

Wykład "WdWK - wieloprocesowość.pdf" slajd 11

---

- Level 0:
- Level 1:
- Level 2:
- Level 3:

## Wyjaśnij czym charakteryzują się rozkazy uprzywilejowane oraz podaj ich przykłady.

Wykład "WdWK - wieloprocesowość.pdf" slajd 12

---

Jest to zbiór rozkazów kontrolujących działanie systemu (np. ładowanie rejestrów). Mogą być wykonane jedynie gdy CPL wynosi 0 (najbardziej uprzywilejowany). W przypadku wykonania przy innym CPL niż 0, następuje wyjątek #GP (General Protection Exception).

Przykłady takich instrukcji:

- mov
- invd
- wbinvd
- hlt
- rdtsc

## Wymień fazy realizacji procesu

Wykład "WdWK - wieloprocesowość.pdf" slajd 13

---

1. uaktywnienie - przydział czasu procesora
2. start - odtworzenie kontekstu
3. wykonanie - synchronizacja
4. wstrzymanie - przechowanie kontestu, zwolnienie procesora

## Wytłumacz czym jest szeregowanie

Wykład "WdWK - wieloprocesowość.pdf" slajd 13

---

Szeregowanie zadań to kolejność wykonania procesów.

Typy kolejek:

- krótkoterminowa - procesy aktywne, często wykonywane
- średnioterminowa - procesy aktywne, rzadko wykonywane
- długoterminowa - procesy uśpione

## Wytłumacz czym jest przerwanie

Wykład "WdWK - wieloprocesowość.pdf" slajd 13

---

Przerwanie to sygnalizacja zdarzenia w środowisku procesów, które wymaga obsługi programowej

Przykłady:

- żądanie komunikacji
- wystąpienie błędu
- upływ czasu

## Przedstaw typy kolejek (w szeregowaniu zadań)

Wykład "WdWK - wieloprocesowość.pdf" slajd 13

---

Typy kolejek:

- krótkoterminowa - procesy aktywne, często wykonywane
- średnioterminowa - procesy aktywne, rzadko wykonywane
- długoterminowa - procesy uśpione

## Przedstaw krótko model procesowy (rozszerzony)

## Przedstaw kolejność wykonania procesów

1. obsługa wyjątków - utrzymanie integralności systemu
2. obsługa wejścia/wyjścia - funkcje krytyczne względem czasu
3. zadania nadzoru - zarządzanie procesami i pamięcią
4. zadania użytkowników (user jobs)
5. zdarzenia asynchroniczne - przerwania zewnętrzne
6. zdarzenia synchroniczne - wywołania systemowe, pułapka, wyjątek

## W jaki sposób identyfikowany jest obiekt w pamięci?

Wykład "WdWK - wieloprocesowość.pdf" slajd 17

---

Przy pomocy identyfikatora procesu oraz adresu logicznego

Taka przestrzeń adresowa jest wirtualna (istnieje jedynie jako koncepcja)

## Ile procesów jednocześnie może być obsługiwanych przez CPU w architekturze x86?

Wykład "WdWK - wieloprocesowość.pdf" slajd 19

---

Tylko 1 proces może być tymczasowym użytkownikiem procesora.
Pamięć główna odwzorowuje pamięć procesu aktywnego

## W jaki sposób jest zabezpiecznay dostęp do pamięci procesu?

Wykład "WdWK - wieloprocesowość.pdf" slajd 20

---

## Wymień funkcje zarządzania pamięcią

Wykład "WdWK - wieloprocesowość.pdf" slajd 21

---

## Wytłumacz ideę przezroczystostej organizacji pamięci fizycznej i logicznej

Wykład "WdWK - wieloprocesowość.pdf" slajd 21

---

## Opisz krótko czym jest pamięć wirtualna?

Wykład "WdWK - wieloprocesowość.pdf" slajd 22, 23, 24

---

## Przedstaw krótko kolejne kroki translacji adresu (opis odwzorowania)

Wykład "WdWK - wieloprocesowość.pdf" slajd 25

---

## Czym jest zbiór roboczy i jaki ma związek z efektem szamotania

Wykład "WdWK - wieloprocesowość.pdf" slajd 26

---

## Czy odwzorowanie częściowe pamięci procesu (przestrzeni wirtualnej) w pamięci operacyjnej jest wystarczające?

Wykład "WdWK - wieloprocesowość.pdf" slajd 27

---

Tak, ponieważ wynika to z lokalności odwołań (lokalność czasowa oraz przestrzenna).

## Czy jest możliwe bezkonfliktowe jednoczesne odwzorowanie pamięci kilku procesów?

Wykład "WdWK - wieloprocesowość.pdf" slajd 27

---

Tak, o ile możliwe jest w danym przypadku oszacowanie przeciętnego zapotrzebowania procesu na pamięć fizyczną (Prawo Little?)

## Opisz krótko czym są oraz jak są przydzielane partycje procesów

Wykład "WdWK - wieloprocesowość.pdf" slajd 27, 28

---

Partycja - część pamięci głównej przydzielonej procesowi. Rozmiar określony jako całkowita wielokrotność bloków o ustalonej wielkości (ramki stron), które przydzielone są statycznie bądź dynamicznie.

## Wyjaśnij pojęcie partycji rozproszonej.

Wykład "WdWK - wieloprocesowość.pdf" slajd 29

---

Jest to partycja złożona z niekolejnych bloków pamięci (ramek stron), co jest możliwe dzięki stronicowaniu.

## Wyjasnij czym jest adres logiczny oraz liniowy

Wykład "WdWK - wieloprocesowość.pdf" slajd 32, 33

---

## Wyjasnij jak zorganizowana jest segmentacja w architekturze x86

Wykład "WdWK - wieloprocesowość.pdf" slajd 33-40

---

## Krótko przedstaw czym są rejestry segementowe oraz wyjaśnij które z nich muszą być załadowane poprawnymi selektorami segmentu przy wykonaniu?

Wykład "WdWK - wieloprocesowość.pdf" slajd 33-40

---

Zadaniem rejestrów segmentowych jest przede wszystkim usprawnienie procesu translacji adresu poprzez redukcję liczby cykli potrzebnych do odczytu danych deskryptora segmentu. W architekturze x86 jest ich 6, a każdy z nich przechowuje wyspecjalizowany typ referencji pamięciowej. Te najbardziej kluczowe z nich to:

- CS (Code Segment)
- DS (Data Segment)
- SS (Stack Segment)

## Wytłumacz pojęcie "Shadow registers".

Wykład "WdWK - wieloprocesowość.pdf" slajd 33-40

---

Każdy rejestr segmentowy składa się z części widocznej i ukrytej. Ta druga często jest określana właśnie terminem "Descriptor cache" bądź "Shadow register". Podczas ładowania widocznej części rejestru ładowana jest również ta ukryta, która zawiera informacje z deskryptora segmentu wskazywanego przez selektor segmentu. Są to:

- adres bazowy
- limit segmentu
- prawa dostępu do segmentu

## Wyjasnij jak zorganizowane jest stronicowanie w architekturze x86

Wykład "WdWK - wieloprocesowość.pdf" slajd 41-45

---

## Wyjasnij pojęcie pamięci podręcznej tablicy stron (TLB)

Wykład "WdWK - wieloprocesowość.pdf" slajd 46-48

---

Bufor translacji antycypacji adresu / TLB (ang. Translation Lookaside
Buffer) - pamięć podręczna, która przechowuje przemapowanie z
adresów wirtualnych do adresów fizycznych. W tym buforze znajduje się
końcowy wynik przejścia po tych wszystkich tablicach dla określonej części
adresu.

## Wyjasnij czym jest Transparent Hugepage Support (THP)

Wykład "WdWK - wieloprocesowość.pdf" slajd 52

---

## Wyjasnij czym jest Odwrócona Tablica Stron

Wykład "WdWK - wieloprocesowość.pdf" slajd 55

---

## ...

## Wyjasnij czym jest Kontekst Procesu

Wykład "WdWK - wieloprocesowość.pdf" slajd 63-67

---

## Task Management

Wykład "WdWK - wieloprocesowość.pdf" slajd 68-70

---

## ...
