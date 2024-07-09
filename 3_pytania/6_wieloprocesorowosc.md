# Wieloprocesorowość

## Jakie są zadania sterowników urządzeń?

- Buforowanie (kolejkowanie) poleceń logicznych.
- Zmiana porządku poleceń w celu poprawy przepustowości transmisji.
- Zmiana logicznych adresów urządzeń i bloków danych na adresy fizyczne.
- Obsługa błędów transmisji

## Prawo amdahla

przyrost wydajnosci jest proporcjonalny do pierwiastka z liczby rdzeni

## jakie są powszechnie używane typy połaczeń rdzeni

- pierscien
- dwuwymiarowa siatka
- macierz połączeń bezpośrednich
- magistrala

## Jakie są funkcje użytkownika w oprogramowaniu we/wy?

- Zmiana symbolicznej nazwy urządzenia na nazwę logiczną.
- Przeformatowanie danych na postać wymaganą przez urządzenie.
- Przydział i zwolnienie przydziału pamięci.

## Czym jest procesor wielordzeniowy?

- Element obliczeniowy z dwoma lub większą liczbą niezależnych jednostek przetwarzających - rdzeni (ang. cores).

## Co obsługują rdzenie procesora wielordzeniowego?

- Różne zbiory instrukcji (np. AMD Accelerated Processing Unit).
- Te same zbiory instrukcji z różną wydajnością i poborem energii (np. ARM big.little).

## Jakie są rodzaje transakcji na magistrali multipleksowanej?

- Zapis (write), pojedynczy lub blokowy (burst mode).
- Odczyt (read), pojedynczy lub blokowy (burst mode).
- Zapis po odczycie i modyfikacji (read-modify-write).
- Odczyt po zapisie (write-after-read).

## Jakie są cechy adresowania zbiorowego?

- Rozgłaszanie (ang. broadcast) – wysyłanie informacji jednocześnie do wielu odbiorców.
- Wywołanie (ang. broadcall) – identyfikacja źródła lub źródeł sygnału.
- Jednoczesny odbiór informacji z wielu źródeł.

## Czym jest arbitraż statyczny?

- Cykliczne przejmowanie magistrali przez zarządców.

## Czym jest arbitraż dynamiczny?

- Przydzielanie magistrali zgodnie z zapotrzebowaniami.

## Jakie są problemy arbitrażu?

- Realizowane centralnie lub lokalnie, wymagają trzech sygnałów: żądania dostępu, gwarancji - potwierdzenia dostępu i zajętości magistrali.
- Zgłoszenia żądań mogą być: dzielone, przekazywane w łańcuchach zgłoszeń typu daisy-chain.
- Niezawodność - zapewnienie satysfakcjonującej obsługi błędów, czyli wykrywanie niesprawności sprzętu sygnalizowanie błędów transmisji.

## Jakie są rodzaje błędów arbitrażu?

- Błędy adresowania – naruszenie reguł dostępu lub adres „donikąd”.
- Błędy danych – kody korekcyjne.
- Błędy arbitrażu – limitowanie czasu potwierdzenia.

## Jakie są typy sterowania urządzeniami (mikrokontrolerami)?

- Programowanie sterownika (wysyłanie poleceń).
- Testowanie sterownika.
- Obsługa przerwań sygnalizowanych przez urządzenia.
- Obsługa błędów urządzeń
  ##Jakie są funkcje użytkownika w oprogramowaniu we/wy?
- Zmiana symbolicznej nazwy urządzenia na nazwę logiczną.
- Przeformatowanie danych na postać wymaganą przez urządzenie.
- Przydział i zwolnienie przydziału pamięci.

## Czym jest procesor wielordzeniowy?

- Element obliczeniowy z dwoma lub większą liczbą niezależnych jednostek przetwarzających - rdzeni (ang. cores).

## Co obsługują rdzenie procesora wielordzeniowego?

- Różne zbiory instrukcji (np. AMD Accelerated Processing Unit).
- Te same zbiory instrukcji z różną wydajnością i poborem energii (np. ARM big.little).

## Jakie są rodzaje transakcji na magistrali multipleksowanej?

- Zapis (write), pojedynczy lub blokowy (burst mode).
- Odczyt (read), pojedynczy lub blokowy (burst mode).
- Zapis po odczycie i modyfikacji (read-modify-write).
- Odczyt po zapisie (write-after-read).

## Jakie są cechy adresowania zbiorowego?

- Rozgłaszanie (ang. broadcast) – wysyłanie informacji jednocześnie do wielu odbiorców.
- Wywołanie (ang. broadcall) – identyfikacja źródła lub źródeł sygnału.
- Jednoczesny odbiór informacji z wielu źródeł.

## Czym jest arbitraż statyczny?

- Cykliczne przejmowanie magistrali przez zarządców.

## Czym jest arbitraż dynamiczny?

- Przydzielanie magistrali zgodnie z zapotrzebowaniami.

## Jakie są problemy arbitrażu?

- Realizowane centralnie lub lokalnie, wymagają trzech sygnałów: żądania dostępu, gwarancji - potwierdzenia dostępu i zajętości magistrali.
- Zgłoszenia żądań mogą być: dzielone, przekazywane w łańcuchach zgłoszeń typu daisy-chain.
- Niezawodność - zapewnienie satysfakcjonującej obsługi błędów, czyli wykrywanie niesprawności sprzętu sygnalizowanie błędów transmisji.

## Jakie są rodzaje błędów arbitrażu?

- Błędy adresowania – naruszenie reguł dostępu lub adres „donikąd”.
- Błędy danych – kody korekcyjne.
- Błędy arbitrażu – limitowanie czasu potwierdzenia.

## jakie jest prawo gordona moorea?

"Co 18 miesięcy podwaja się gęstość upakowania układów VLSI oraz osiąglana szybkość przełączania"

## Czym jest raid 0 oraz ile dysków może się wyjebać?

Zapis i doczyt może być wykonywany jednocześnie na każdym dysku ale jak jeden dysk sie wykurwi to koniec. Masz dostępne tyle pamięci ile masz dysków

## Czym jest raid 1 oraz ile dysków może się wyjebać?

Zapis następuje jednoczesnie na obu dyskach na raz odczyt może nastąpić z jednego z dwóch lub obu dysków. Jeden dysk może się wyjebać bez strat danych ale maksymalnie posiada tyle pamięci ile najmniejszy dysk w raidzie. Minimalnie 2 dyski

## Czym jest raid 4 oraz ile dysków może się wyjebać?

Prędkość zapisu jest ograniczona prez konieczność tworzenia bitów parzystości. Wszystkie bity parzystości są na jednym dysku. Minimalnie 3 dyski. Możesz stacić 1 dysk bez utraty danych dostępna przestrzeń to n-1 dysków.

## Czym jest raid 5 oraz ile dysków może się wyjebać?

Zapis wymaga aktualizacji parzystosci.Bity parzystości są na wszystkich dyskach Minimalnie 3 dyski. Możesz stacić 1 dysk bez utraty danych dostępna przestrzeń to n-1 dysków.

## problemy w przetwarzaniu superskalarnym

- zależność dancyh
  - WAR
  - WAW
  - RAW
- zależność proceduralna
  - rozgałęzienia
  - procedury i powroty
- konflikt zasobów
  - dostęp do pamięci
  - instrukcje czasochłonne

## Jakie są klasy przetwarzania

SISD single instruction single data

- procesor pojedynczy
  SIMD single instruction multiple data
- procesor wektorowy/macierzowy
  MISD multiple instruction single data
- procesor wektorowy
  MIMD - multiple instruction multiple data

## jaka jest klasyfikacja magistral

- lokalna
- systemowa
- sprzęgająca
