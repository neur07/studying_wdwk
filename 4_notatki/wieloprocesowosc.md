# Wieloprocesowość

## Program Sekwencyjny

### Własności Poprawności

- **Poprawność**: Gwarancja, że program sekwencyjny daje poprawne wyniki przy założeniu, że instrukcje są wykonywane w odpowiedniej kolejności.
- **Wymagania**: Precyzyjnie określona kolejność wykonywania instrukcji oraz deterministyczność wyników.

## Procesy Współbieżne

### Poprawność Procesu Współbieżnego

- **Poprawność procesu współbieżnego**: Osiągnięcie właściwego wyniku mimo potencjalnych interferencji między procesami.

## System Operacyjny

### Funkcje

- **Funkcje systemu operacyjnego**: Zarządzanie zasobami, zarządzanie procesami, zarządzanie pamięcią, zarządzanie plikami, interfejs użytkownika.

### Warunki

- **Warunki**: Ochrona zasobów, bezpieczeństwo, stabilność, wydajność.

### Ochrona Procesu

- **Ochrona procesu**: Mechanizmy zapewniające, że procesy nie wpływają negatywnie na siebie nawzajem, np. poprzez odizolowanie pamięci.

## Tryby Operacyjne

- **Tryby operacyjne (Operation Modes)**: Różne poziomy uprzywilejowania, takie jak tryb użytkownika i tryb jądra, które kontrolują dostęp do zasobów systemowych.

## Modele Procesu

- **Modele procesu**: Różne sposoby zarządzania procesami, takie jak model procesów współbieżnych, model wątków itp.

## Poziomy Uprzywilejowania

- **Poziomy uprzywilejowania**: Hierarchia uprawnień, które kontrolują dostęp do zasobów systemowych, np. poziomy ring w architekturze x86.

## Pamięć Wielu Procesów

### Pamięć Wirtualna

- **Pamięć wirtualna**: Mechanizm pozwalający na używanie większej ilości pamięci niż fizycznie dostępna poprzez odwzorowanie adresów logicznych na adresy fizyczne.

### Odwzorowanie w Przestrzeni Operacyjnej

- **Odwzorowanie w przestrzeni operacyjnej**: Mapowanie pamięci wirtualnej na fizyczną przestrzeń adresową.

### Przestrzeń Wirtualna

- **Przestrzeń wirtualna**: Logiczna przestrzeń adresowa udostępniana procesowi, niezależnie od rzeczywistej fizycznej pamięci.

### Ochrona Pamięci Procesu

- **Ochrona pamięci procesu**: Mechanizmy zapewniające, że jeden proces nie może bezpośrednio ingerować w pamięć innego procesu.

## Zarządzanie Pamięcią

### Funkcje Zarządzania Pamięcią

- **Funkcje zarządzania pamięcią**: Alokacja i dealokacja pamięci, ochrona pamięci, współdzielenie pamięci, stronicowanie.

### Koncepcja Pamięci Wirtualnej a Hierarchia Pamięci

- **Pamięć wirtualna a hierarchia pamięci**: Pamięć wirtualna jako element hierarchii pamięci, pozwalający na efektywne zarządzanie różnymi poziomami pamięci.

### Translacja Adresu

- **Translacja adresu**: Proces przekształcania adresów logicznych na fizyczne.

### Model Zbioru Roboczego

- **Model zbioru roboczego**: Koncepcja zarządzania pamięcią, która określa, które strony pamięci są aktualnie używane przez proces.

### Bloki Przestrzeni Wirtualnej

- **Bloki przestrzeni wirtualnej**: Podział przestrzeni adresowej na mniejsze, zarządzalne jednostki.

### Partycje

- **Partycje**: Podziały przestrzeni adresowej na odrębne segmenty.

### Fragmentacja

- **Fragmentacja**: Problem rozproszonej pamięci nieużywanej, który może prowadzić do nieefektywnego wykorzystania pamięci.

### Segmentacja

- **Segmentacja**: Podział przestrzeni adresowej na segmenty o różnej wielkości i funkcji.

### Stronicowanie

- **Stronicowanie**: Mechanizm zarządzania pamięcią polegający na podziale przestrzeni adresowej na strony o stałej wielkości.

### Adresy Logiczne i Liniowe

- **Adresy logiczne**: Adresy używane przez programy.
- **Adresy liniowe**: Adresy wynikające z translacji logicznych adresów na adresy fizyczne.

### TLBS

- **TLB (Translation Lookaside Buffer)**: Pamięć podręczna używana do przyspieszenia translacji adresów wirtualnych na fizyczne.

### L1, L2, HPTB

- **L1, L2**: Różne poziomy pamięci podręcznej.
- **HPTB (Hierarchical Page Table Buffer)**: Bufor tablicy stron używany do zarządzania dużymi przestrzeniami adresowymi.

### Koszty

- **Koszty**: Zasoby potrzebne do zarządzania pamięcią wirtualną, takie jak czas procesora i pamięć.

### HugeTLB

- **HugeTLB**: Technika używania dużych stron pamięci w celu zredukowania narzutu związanego z zarządzaniem stronami.

### ASLR

- **ASLR (Address Space Layout Randomization)**: Technika zabezpieczeń polegająca na losowym rozmieszczeniu przestrzeni adresowej w celu utrudnienia ataków.

### Kontekst Procesora, Pamięci

- **Kontekst procesora**: Stan rejestrów i innych elementów procesora dla danego procesu.
- **Kontekst pamięci**: Stan pamięci używanej przez dany proces.

### Synchronizacja

- **Synchronizacja**: Mechanizmy zapewniające poprawność współdziałania procesów, takie jak semafory i mutexy.

## Pamięć Współdzielona

### Wyścig Danych

- **Wyścig danych (Race Condition)**: Problem wynikający z niekontrolowanego dostępu do współdzielonej pamięci przez wiele procesów.

### Fałszywe Współdzielenie

- **Fałszywe współdzielenie (False Sharing)**: Problem wynikający z niezamierzonego współdzielenia danych przez różne procesy.

### Współzawodnictwo

- **Współzawodnictwo (Contention)**: Konflikty wynikające z jednoczesnego dostępu do współdzielonych zasobów.

### Wzajemne Wykluczenie

- **Wzajemne wykluczenie (Mutual Exclusion)**: Technika zapewniająca, że tylko jeden proces może mieć dostęp do współdzielonego zasobu w danym czasie.

### Schemat Blokady

- **Schemat blokady**: Mechanizmy blokowania zasobów w celu zapewnienia wzajemnego wykluczenia.

### Mechanizmy Synchronizacji

- **Mechanizmy synchronizacji**: Narzędzia takie jak semafory, mutexy, bariery używane do zarządzania współdzielonymi zasobami.

### LOCK, CMPXCHG, XADD

- **LOCK**: Instrukcja blokująca dostęp do zasobu.
- **CMPXCHG (Compare and Exchange)**: Instrukcja porównująca i zamieniająca wartość atomowo.
- **XADD (Exchange and Add)**: Instrukcja zamieniająca i dodająca wartość atomowo.

### Aktywne Oczekiwanie

- **Aktywne oczekiwanie (Busy-Waiting)**: Technika czekania na zasób poprzez ciągłe sprawdzanie jego dostępności.

## Blokada Wirująca + MESI

### Modele Spójności

- **Modele spójności (Consistency Models)**: Reguły określające, jak i kiedy zmiany w pamięci są widoczne dla procesów.

### Ordering

- **Ordering**: Kolejność wykonywania operacji pamięciowych w systemie wieloprocesorowym.

### Instrukcje Serializujące

- **Instrukcje serializujące**: Instrukcje zapewniające, że wszystkie poprzednie operacje są zakończone przed rozpoczęciem nowych.

### Przerwania i Wyjątki

- **Przerwania i wyjątki**: Mechanizmy obsługi zdarzeń asynchronicznych i błędów w systemie.

### MHI, NMI

- **MHI (Maskable Hardware Interrupt)**: Przerwanie sprzętowe, które może być wyłączone przez procesor.
- **NMI (Non-Maskable Interrupt)**: Przerwanie sprzętowe, które nie może być wyłączone przez procesor.

### Klasyfikacje Wyjątków

- **Klasyfikacje wyjątków**: Różne typy wyjątków, takie jak błędy strony, pr

zerwania sprzętowe, wyjątki programowe.

### Obsługa Przerwań

- **Obsługa przerwań**: Mechanizmy zarządzania przerwaniami, takie jak wektoryzacja i dystrybucja przerwań.

### Identyfikacja, Odpytywanie

- **Identyfikacja i odpytywanie**: Techniki identyfikacji źródła przerwania i jego obsługi.

### Wektoryzacja

- **Wektoryzacja**: Mechanizm przypisywania unikalnych identyfikatorów przerwaniom.

### APIC

- **APIC (Advanced Programmable Interrupt Controller)**: Zaawansowany kontroler przerwań programowalnych używany w systemach wieloprocesorowych.

### Dystrybucja

- **Dystrybucja przerwań**: Mechanizmy rozdzielania przerwań pomiędzy różne procesory w systemie.

### IRET, ITETD

- **IRET (Interrupt Return)**: Instrukcja powrotu z obsługi przerwania.
- **ITETD**: Niezdefiniowane pojęcie, może być literówką lub skrótem związanym z obsługą przerwań.
