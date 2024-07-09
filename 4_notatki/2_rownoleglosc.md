# Równoległość Drobnoziarnista

## Równoległość Drobnoziarnista (Fine-Grained Parallelism)

- **Równoległość drobnoziarnista**: Technika polegająca na wykonywaniu wielu małych, niezależnych zadań jednocześnie. Przykłady zastosowań to przetwarzanie potokowe oraz procesory superskalarne.

## Poziomy Równoległości

- **Poziomy równoległości**: Hierarchia różnych stopni równoległości, od drobnoziarnistej (fine-grained) po gruboziarnistą (coarse-grained).

## Przetwarzanie Potokowe

- **Przetwarzanie potokowe (Pipelining)**: Technika przetwarzania polegająca na podziale zadania na mniejsze etapy, które są wykonywane równocześnie przez różne części procesora.

## Procesory Superskalarne

- **Procesory superskalarne**: Procesory zdolne do jednoczesnego wykonywania wielu instrukcji w jednym cyklu zegara dzięki wielu jednostkom wykonawczym.

## Maszyny Masowo-Równoległe

- **Maszyny masowo-równoległe (Massively Parallel Machines)**: Systemy komputerowe zdolne do wykonywania bardzo wielu operacji jednocześnie, często wykorzystujące wiele rdzeni (many-core).

## Równoległość Gruboziarnista

- **Równoległość gruboziarnista (Massively Parallel, Many-Core)**: Typ równoległości, gdzie zadania są podzielone na większe, niezależne segmenty wykonywane równocześnie.

## Równoległość Średnioziarnista

- **Równoległość średnioziarnista**: Kompromis między drobnoziarnistą a gruboziarnistą równoległością, wykorzystujący średniej wielkości zadania.

## Organizacja Komputera

### System Architecture (HSA), Microarchitecture (uarch), Computer Organization

- **System architecture (HSA)**: Ogólna architektura systemu komputerowego.
- **Microarchitecture (uarch)**: Szczegółowa organizacja i projektowanie wewnętrznych komponentów procesora.
- **Computer organization**: Sposób, w jaki komponenty komputerowe są zorganizowane i współdziałają ze sobą.

### Struktura Logicza Realizująca ISA

- **ISA (Instruction Set Architecture)**: Zbiór instrukcji, które procesor może wykonać, oraz sposób ich implementacji w sprzęcie.

### Cykl Rozkazowy

- **Cykl rozkazowy**: Sekwencja kroków, które procesor wykonuje, aby wykonać jedną instrukcję (pobranie, dekodowanie, wykonanie, zapis).

## Koncepcja Przetwarzania Potokowego

### Etapy Przetwarzania, Relacje Między Nimi, Własności

- **Etapy przetwarzania**: Fazy potoku, takie jak pobranie instrukcji, dekodowanie, wykonanie, zapis wyników.
- **Relacje między etapami**: Każdy etap jest niezależny i może działać równolegle z innymi etapami.
- **Własności**: Przetwarzanie potokowe zwiększa wydajność poprzez równoczesne wykonywanie wielu instrukcji.

### Powielenie Układów Funkcjonalnych

- **Powielenie układów funkcjonalnych**: Zwiększenie liczby jednostek wykonawczych w procesorze, aby umożliwić równoczesne wykonywanie wielu operacji.

### Kwantyzacja Cyklu

- **Kwantyzacja cyklu**: Podział cyklu zegara na mniejsze segmenty w celu zwiększenia precyzji i efektywności przetwarzania.

### Przepływ Danych

- **Przepływ danych**: Ruch danych przez różne etapy potoku przetwarzania.

### Architektura R/M

- **Architektura R/M**: Różne podejścia do projektowania procesorów, takie jak CISC (Complex Instruction Set Computing) i RISC (Reduced Instruction Set Computing).

### Ścieżki Przepływu Danych

- **Ścieżki przepływu danych**: Drogi, którymi dane poruszają się w procesorze podczas wykonywania instrukcji.

### Organizacja Procesora Potokowego

- **Organizacja procesora potokowego**: Struktura i zasady działania procesora z przetwarzaniem potokowym.

## Architektura Klasyczna

### CISC

- **CISC (Complex Instruction Set Computing)**: Architektura komputerowa z dużą liczbą złożonych instrukcji.
  - **Lista rozkazów**: Długa lista skomplikowanych instrukcji.
  - **Organizacja**: Złożona struktura procesora.
  - **Skutki**: Mniejsze zużycie pamięci, ale większa złożoność sprzętu.

### RISC

- **RISC (Reduced Instruction Set Computing)**: Architektura z ograniczoną liczbą prostych instrukcji.
  - **Lista rozkazów**: Krótsza lista prostych instrukcji.
  - **Organizacja**: Prostsza struktura procesora.
  - **Skutki**: Większa wydajność, mniejsza złożoność sprzętu.

### Ewolucja CISC -> RISC

- **Ewolucja CISC -> RISC**: Proces przejścia od złożonych instrukcji do prostszych, bardziej efektywnych instrukcji w celu zwiększenia wydajności.

## Przestoje (Blokady) Potoku

### Skutki Konfliktów Przetwarzania

- **Przestoje (blokady) potoku**: Opóźnienia w przetwarzaniu spowodowane konfliktami.

### Konflikty Przetwarzania

- **Danych**: Konflikty wynikające z zależności między danymi.
- **Strukturalne**: Konflikty wynikające z ograniczeń sprzętowych.
- **Sterowania**: Konflikty wynikające z rozgałęzień w kodzie programu.

### Potok Statyczny i Dynamiczny

- **Potok statyczny**: Potok z ustaloną sekwencją etapów.
- **Potok dynamiczny**: Potok z elastyczną sekwencją etapów, dostosowującą się do bieżących warunków.

### Łagodzenie Skutków Konfliktów

- **Skok opóźniony**: Technika opóźniająca wykonanie instrukcji skoku, aby zminimalizować przestoje.
- **Prognoza rozgałęzień**: Metody przewidywania kierunku skoków w kodzie programu.
  - **Statyczna**: Stała prognoza kierunku skoku.
  - **Dynamiczna**: Prognoza oparta na analizie wcześniejszych skoków.

### Wielomagistralowy Dostęp do Pliku Rejestrowego

- **Wielomagistralowy dostęp**: Jednoczesny dostęp do rejestrów procesora przez wiele jednostek wykonawczych.

### Niekolejne Wykonania

- **Niekolejne wykonania**: Technika wykonywania instrukcji w innej kolejności niż w kodzie programu, aby zminimalizować przestoje.

### Algorytm Tomasulo

- **Algorytm Tomasulo**: Metoda dynamicznego planowania i wykonywania instrukcji w procesorach, umożliwiająca równoległe przetwarzanie bezkonfliktowe.

### Przetwarzanie Wektorowe

- **SSE (Streaming SIMD Extensions)**: Zestaw instrukcji umożliwiających równoległe przetwarzanie danych wektorowych.
