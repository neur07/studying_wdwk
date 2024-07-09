# Pamięć Podręczna

## Bariera pamięci

- **Bariera pamięci**: Mechanizm synchronizacyjny, który zapewnia poprawność dostępu do pamięci w systemach wieloprocesorowych.

## Architektura von Neumanna

- **Von Neumann**: Model architektury komputera, w którym pamięć przechowuje zarówno dane, jak i programy.

## Zasada lokalności

- **Zasada lokalności**: Kluczowa zasada projektowania pamięci podręcznej, która opiera się na obserwacji, że programy komputerowe mają tendencję do dostępu do danych i instrukcji w sposób lokalny.

### Typy lokalności

- **Lokalność przestrzenna**: Dane znajdujące się blisko siebie są często używane w krótkim odstępie czasu.
- **Lokalność czasowa**: Dane, które były niedawno używane, mają dużą szansę być używane ponownie w niedalekiej przyszłości.

## Zasady użycia buforów

- **Bufory pamięci**: Pamięć tymczasowa służąca do przechowywania danych między różnymi poziomami hierarchii pamięci.

## Organizacja pamięci podręcznej

### Organizacja sekwencyjna, blokowo-skojarzeniowa

- **Organizacja sekwencyjna**: Dane przechowywane w kolejnych adresach pamięci.
- **Organizacja blokowo-skojarzeniowa**: Dane przechowywane w blokach, które mogą być umieszczone w dowolnym miejscu w pamięci podręcznej.

### Współdziałanie pamięci podręcznej z procesorem

- **Odczyt**: Procesor sprawdza, czy dane są dostępne w pamięci podręcznej.
- **Zapis**: Procesor zapisuje dane do pamięci podręcznej, a następnie do głównej pamięci.

### Współpraca bufora cache z procesorem i pamięcią

- **Wyszukiwanie danych w pamięci podręcznej**: Procesor przeszukuje pamięć podręczną w celu znalezienia potrzebnych danych.

## Organizacja danych w pamięci podręcznej

- **Linia (blok danych)**: Jednostka danych w pamięci podręcznej.
- **Dane bloku**: Dane przechowywane w pojedynczej linii pamięci podręcznej.
- **Identyfikator słowa**: Adres pamięci operacyjnej.
- **Wpasowanie bloków w przestrzeni adresowej pamięci operacyjnej**: Proces dopasowywania bloków danych do odpowiednich adresów pamięci.

## Organizacja odwzorowania danych w pamięci podręcznej

### Typy odwzorowań

- **Całkowicie skojarzeniowe**: Blok może być umieszczony w dowolnym miejscu w pamięci podręcznej.
- **Bezpośrednie z przeplotem**: Każdy blok ma jedno konkretne miejsce w pamięci podręcznej.
- **Bez przeplotu**: Bloki są przypisywane sekwencyjnie do linii pamięci podręcznej.

### Grupy skojarzeniowe (wielodrożne)

- **Z przeplotem**: Dane są rozproszone między różnymi bankami pamięci.
- **Bez przeplotu**: Dane są przypisane do jednego konkretnego banku pamięci.

## Obsługa pamięci podręcznej

### Operacje

- **Line Invalidation**: Inwalidacja linii danych w pamięci podręcznej.
- **Line Fill**: Wypełnianie linii pamięci podręcznej danymi.
- **Read**: Odczyt danych z pamięci podręcznej.
- **Write**: Zapis danych do pamięci podręcznej.
- **Hit**: Znalezienie danych w pamięci podręcznej.
- **Miss**: Nieznalezienie danych w pamięci podręcznej.

### Aktualizacja zawartości bufora cache

- **Bufory zapisu**: Bufory używane do tymczasowego przechowywania danych przed ich zapisaniem do pamięci głównej.

### Instrukcje strumieniowe

- **Instrukcje strumieniowe**: Instrukcje służące do przyspieszania operacji na dużych zestawach danych.

### Kategorie chybień

- **Redukcja chybień**: Techniki zmniejszania liczby nieudanych odczytów z pamięci podręcznej.

## Zarządzanie pamięcią podręczną

### Schematy wymiany linii

- **Intensywność pobrań uprzedzających**: Poziom agresywności wstępnego pobierania danych do pamięci podręcznej.

### Cache Management Instructions

- **Cache Management Instructions**: Instrukcje zarządzające działaniem pamięci podręcznej.

### Skuteczność buforów cache

- **Charakterystyki skuteczności**: Parametry określające efektywność pamięci podręcznej.

## Pamięć wielopoziomowa

### Hierarchia pamięci wielopoziomowej

- **Wielopoziomowy bufor**: Bufory pamięci na różnych poziomach hierarchii.
- **Organizacja hierarchiczna (inkluzywna)**: Każdy poziom pamięci podręcznej zawiera dane z niższych poziomów.
- **Organizacja równoległa (nieinkluzywna)**: Poziomy pamięci podręcznej działają niezależnie.

### Problem spójności

- **Zintegrowany model spójności pamięci podręcznej (MESI)**: Protokół zapewniający spójność danych w pamięci podręcznej.

### Strategia zapisu jednorazowego

- **Strategia zapisu jednorazowego**: Dane są zapisywane bezpośrednio do pamięci głównej, z pominięciem pamięci podręcznej.

### Pamięć notatnikowa

- **Pamięć notatnikowa**: Specjalny rodzaj pamięci podręcznej przechowujący notatki i tymczasowe dane.

### Blokowanie pamięci podręcznej

- **Blokowanie pamięci podręcznej**: Techniki zabezpieczania danych w pamięci podręcznej przed nadpisaniem.

## Podsumowanie

Pamięć podręczna jest kluczowym elementem nowoczesnych systemów komputerowych, zwiększającym wydajność poprzez redukcję czasu dostępu do danych i zmniejszenie obciążenia pamięci głównej. Rozumienie zasad jej działania, organizacji i zarządzania jest niezbędne do efektywnego projektowania i optymalizacji systemów komputerowych.
