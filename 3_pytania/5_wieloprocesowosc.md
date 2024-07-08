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

##

## Opisz krótko czym są oraz jak są przydzielane partycje procesów
