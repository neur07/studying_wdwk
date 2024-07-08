# Pamięć podręczna

## Wymień elementy komputera z programem przechowywanym

Procesor, Magistrala, Pamięć

## Wyjaśnij pojęcie bariery pamięci

Przepaść między szybkim wzrostem przepustowości/wydajności procesora
a ograniczonym wzrostem mocy obliczeniowej/wydajności pamięci
na przestrzeni lat

## Czym jest lokalność przestrzenna?

Przesłanka do wykorzystania bufora, wynikająca
z wysokiego prawdopodobieństwa ponownego użycia informacji z
sąsiednich lokalizacji w pamięci.
Dane bloku tworzą zbiór uporządkowany
(lokalność przestrzenna:sąsiedztwo)

## Czym jest lokalność czasowa?

Przesłanka do wykorzystania bufora, wynikająca
z wysokiego prawdopodobieństwa ponownego użycia kodu
w nieodległym czasie
Linie w buforze tworzą zbiór nieuporządkowany
(lokalność czasowa).

## Na czym polega obsługa pamięci podręcznej?

- unieważnianie linii
- wypełnianie linii
- odczyt danej
- zapis danej

## Jakie mechanizmy stosuje się w celu utrzymania spójności danych?

Aktualizacja zawartości bufora cache:

- unieważnienie linii z informacjami nieważnymi
- wypełnienie linii informacjami ważnymi
- wymiana linii gdy brakuje wolnego miejsca w buforze
- zapis w obszarze skopiowanej linii

## Czym różni się zapis skrośny od zapisu lokalnego?

Zapis skrośny(write through WT) zapewnia zgodność wszystkich kopii informacji
i każda zmiana w cache jest odzwierciedlana w pamięci głównej,
a zapis lokalny(copy-back CB) znajomość lokalizacji informacji aktualnej
i zapisy wykonywane najpierw tylko w cache a dane zapisywane
do pamięci głównej gdy linia cache jest wymieniana

## Podsumuj działanie schematów alokacji

Allocate on Write AOW-
gdy na linii(jakiej??) wykonywany jest zapis nieobecny w cache,
ta linia jest ładowana do cache a potem jest zapis,
wcześniejsze ładowanie linii do cache

No Allocate on Write NAOW-
bezpośredni zapis w pamięci głównej gdy linii nie ma w cache,
bez wcześniejszego ładowania linii do cache

## Przedstaw wymagania dla buforu pamięci

- niewidoczny na poziomie ISA
- realizowany na poziomie HSA
- powinien skracać czas wykonania rozkazu
- wykonanie rozkazu nie powinno zależeć od obecności bufora (przezroczystość)
- nie tworzy nowej przestrzeni adresowej
- położony blisko procesora
- szybki dostęp do kopii informacji aktualnie używanych

## Przedstaw sposób organizacji buforu rozkazów oraz pamięci podręcznej

Bufor rozkazów - kolejka rozkazów
Pamięć podręczna - organizacja blokowo-skojarzeniowa, kopia używanych danych

## Wymień rodzaje odwzorowań pamięci cache

- całkowicie skojarzeniowe
- bezpośrednie: z przeplotem, bez przeplotem
- wielodrożne: z przeplotem, bez przeplotu

## Wymień i opisz schematy zarządzania liniami w pamięci podręcznej

Schematy:

- wypełniania pamięci podręcznej:
  odwzorowanie pamięci głównej, losowe, bezpośrednie, wielodrożne
- wymiany linii
  losowy, kolejkowy/FIFO, wg używalności/LRU
- pobierania linii
  wymuszone, uprzedzające

## Wymień i opisz kategorie chybień

-nieuniknione
podczas pierwszej próby dostępu do bloku,
bo nie ma tam ważnych danych
-ograniczona pojemność
zbyt mały bufor, potrzeba usuwania i zastępowania bloków
-konflikt
odwzorowanie bloku może wymagać usunięcia danego bloku,
choć w innych grupach są wolne miejsca
(odwzorowania bezpośrednie i wielodrożne)
(-spójność w systemie wieloprocesorowym)

## Wymień i opisz sposoby redukcji chybień

- zwiększenie rozmiaru linii
- zwiększenie pojemności bufora cache
- bufor welopoziomowy
- unikanie translacji adresu wirtualnego

## Wskaż różnice w odwzorowaniach w buforze wielopoziomowym

Inkluzywne:

- linia bufora L1 ma oryginał w buforze L2
- usunięcie zmodyfikowanej linii bufora L1 wymusza aktualizację oryginału w buforze L2
- usunięcie niezmodyfikowanej linii bufora L1 nie powoduje zmian w buforze L2

Nieinkluzywne:

- linia bufora L1 nie ma kopii w buforze L2
- usunięcie linii bufora L1 wymusza wymianę linii z buforem L2
- usunięcie linii bufora L2 wymusza aktualizację linii w pamięci

## Wyjaśnij parametry wielopoziomowego bufora pamięci podręcznej

Typowe:

- szerokość magistrali danych
- transfer blokowy
- rozmiar strony

L1:

- rozmiar linii
- rozmiar pamięci

L2:

- rozmiar linii
- rozmiar bufora

## Opisz kompletny model MESI i jego funkcję

Po co jest -> to prokół spójności pamięci podręcznej

| Różne | Jednakowe | Dane / zapis |
| ----- | --------- | ------------ |
| I     | S         | skrośny      |
| M     | E         | zwrotny      |

Stany:

- modified M - linia zawiera ważną zmodyfikowaną kopię danych,
  kopia w pamięci głównej nie ważna, żaden inny procesor nie ma tej kopii

- exclusive E - linia zawiera ważną zmodyfikowaną kopię danych, kopia w pamięci głównej też jest ważna poprawna, żaden inny procesor nie ma tej kopii

- shared S -linia zawiera ważną poprawną kopię danych, inne procesory mogą/nie muszą mieć ważnej kopii,

- invalid I - linia zawiera nieważną kopię danych, ważne kopie są w innych procesorach lub pamięci głównej

WT write-through, CB copy-back i WO write-once aktualizują pamięci

WT -> zmiana cache zmienia pamięć główną ->
do shared S przechodzi

CB -> wymiana cache zmiana pamięci głównej ->
w stanie modified M dane aktualizowane tylko w cache,
zarówno read i write powodują przejście M w samego siebie

## Opisz blokowanie pamięci podręcznej

Restrukturyzacja pętli przez dzielenie iteracji na podzadania
mieszczące się w pamięci cache
Zalety:

- zwiększenie lokalności przestrzennej i czasowej
