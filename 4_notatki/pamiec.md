# Pamięć

## Hierarchia pamięci

- **Rejestry**: Najszybszy, najmniejszy poziom pamięci, bezpośrednio połączony z jednostką centralną.
- **Pamięć główna (RAM)**: Szybka pamięć operacyjna, używana do przechowywania danych aktualnie przetwarzanych przez CPU.
- **Pamięć wtórna**: Wolniejsza, większa pamięć przechowująca dane długoterminowo (np. dyski twarde, SSD).
- **Archiwum**: Najwolniejsza, najtańsza pamięć do długoterminowego przechowywania danych (np. taśmy magnetyczne).

## Przepustowość, szybkość przetwarzania (Memory Bottleneck)

- **Przepustowość**: Ilość danych, która może być przetworzona w określonym czasie.
- **Szybkość przetwarzania**: Czas potrzebny na odczyt lub zapis danych.
- Wąskie gardła pamięci wynikają z ograniczeń w przepustowości i szybkości przetwarzania.

## Różne typy pamięci

- **Rejestry**
- **Pamięć główna**
- **Pamięć wtórna**
- **Archiwum**

### Podział ze względu na dostęp

- **RAM (Random Access Memory)**: Pamięć o swobodnym dostępie.
- **SAM (Sequential Access Memory)**: Pamięć o dostępie sekwencyjnym.
- **CAM (Content Addressable Memory)**: Pamięć o dostępie na podstawie zawartości.

## Dostęp swobodny: RAM

### Podział ze względu na trwałość

- **Nieulotna**
  - **ROM (Read-Only Memory)**
  - **NVRAM (Non-Volatile RAM)**
- **Ulotna**
  - **Statyczna (SRAM)**
  - **Dynamiczna (DRAM)**

## Dostęp sekwencyjny: SAM

- **Magnetyczna**: Taśmy magnetyczne.
- **Optyczna**: Dyski CD, DVD.
- **Pamięć o dostępie bezpośrednim (DAM)**: Specjalizowane systemy pamięci sekwencyjnej.

## Budowa / anatomia pamięci

### Pobór mocy w komórkach statycznych i dynamicznych

- **Statyczne (SRAM)**: Mniejszy pobór mocy w stanie bezczynności, wyższy w czasie aktywności.
- **Dynamiczne (DRAM)**: Stały pobór mocy ze względu na konieczność odświeżania danych.

### Matryca pamięci statycznej

- Struktura i organizacja komórek pamięci w SRAM.

### Organizacja i obsługa RAM

- **Fakty DRAM**: Zasady działania, odświeżanie danych.
- **Układ RC**: Elementy elektryczne odpowiedzialne za opóźnienia.
- **Matryca pamięci dynamicznej**: Struktura komórek DRAM.
- **Organizacja i obsługa DRAM**: Zarządzanie odświeżaniem, dostępem do danych.

### Atak młotowy (Rowhammer Attack)

- Technika, która wykorzystuje błędy w DRAM do nieautoryzowanego modyfikowania danych.

### Bank Access Operation

- Mechanizm dostępu do banków pamięci w DRAM.

### Diagram i tabela prawdy

- Diagramy ilustrujące operacje na pamięci.
- Tabele prawdy określające warunki logiczne dla operacji.

### Read Burst Operation

- Sposób sekwencyjnego odczytu danych z pamięci.

### Write Burst Operation

- Sposób sekwencyjnego zapisu danych do pamięci.

### Przebiegi i przepustowość pamięci

- Wpływ różnych operacji na przepustowość pamięci.

### Double Data Rate (DDR), DIMM, SO-DIMM

- **DDR**: Technologia podwójnej szybkości transmisji danych.
- **DIMM**: Moduły pamięci do komputerów stacjonarnych.
- **SO-DIMM**: Mniejsze moduły pamięci do laptopów.

### Parametry DDR

- Cechy techniczne DDR: szybkość, przepustowość, opóźnienia.

### Stride, block size

- Wpływ wzorców dostępu do pamięci na wydajność.

### Parametry czasowe pamięci

- Czas dostępu, opóźnienia, cykle pamięci.

### Prawo Little'a

- Wzór określający zależność między przepustowością, opóźnieniem i liczbą operacji w systemie.

### Anatomia DIMM: Ranks, Banks, Arrays

- Struktura fizyczna i logiczna modułów DIMM.

### Mapowanie adresu fizycznego

- Przypisywanie adresów logicznych do fizycznych lokalizacji w pamięci.

### Pomiary

- Metody i narzędzia do oceny wydajności pamięci.

### STREAM

- Benchmark do testowania przepustowości pamięci.

## Techniki pamięciowe

### Równoległe transakcje

- Metody zwiększania wydajności poprzez równoczesne przetwarzanie wielu operacji.

### Pobieranie uprzedzające

- Techniki przewidywania przyszłych operacji pamięci i wcześniejszego pobierania danych.

### Wzorce dostępu (Memory Access Pattern)

- Analiza i optymalizacja wzorców dostępu do pamięci.

### Kafelkowanie

- Technika optymalizacji pamięci poprzez podział danych na mniejsze bloki.

### Krzywe wypełniające

- Algorytmy porządkujące dostęp do pamięci w celu zwiększenia efektywności.

### Pamięć o dostępie bezpośrednim (DMA)

- Mechanizmy umożliwiające bezpośredni transfer danych między pamięcią a urządzeniami z pominięciem CPU.

### Buforowanie nośnika sekwencyjnego

- Techniki zwiększania wydajności dostępu do pamięci sekwencyjnej poprzez buforowanie danych.

### Prognozowanie zapotrzebowania na dane

- Algorytmy przewidujące przyszłe potrzeby pamięciowe w celu optymalizacji dostępu.

### DMA - sposób użycia, tryby pracy

- Zastosowanie i różne tryby operacji DMA w systemach komputerowych.
