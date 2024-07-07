# Wieloprocesorowość

## Prawa Gordona Moore'a

- **Prawo Moore'a**: Obserwacja, że liczba tranzystorów w układzie scalonym podwaja się co około 18 miesięcy, co prowadzi do wzrostu wydajności komputerów.

## Przetwarzanie Równoległe i Współbieżne

- **Przetwarzanie równoległe**: Wykonywanie wielu operacji jednocześnie przez wiele procesorów lub rdzeni.
- **Przetwarzanie współbieżne**: Wykonywanie wielu zadań, które mogą być przeplatane, ale niekoniecznie wykonywane równocześnie.

## Analiza Różnych Scenariuszy

- Analiza efektywności różnych podejść do przetwarzania równoległego i współbieżnego w różnych kontekstach aplikacyjnych.

## Problemy w Przetwarzaniu Superskalarnym

- **Zależności danych**: Problemy wynikające z konieczności sekwencyjnego wykonywania instrukcji zależnych od siebie.
- **Zależności proceduralne**: Problemy wynikające z konieczności zachowania poprawności proceduralnej.
- **Konflikty zasobów**: Problemy wynikające z ograniczonej dostępności zasobów sprzętowych.

## Bufor Zmiany Kolejności

- Mechanizm pozwalający na dynamiczne zmienianie kolejności wykonywania instrukcji w celu optymalizacji wydajności.

## Taksonomia Flynna

- **SISD (Single Instruction Stream, Single Data Stream)**: Jedna instrukcja operująca na jednym strumieniu danych.
- **SIMD (Single Instruction Stream, Multiple Data Stream)**: Jedna instrukcja operująca na wielu strumieniach danych.
- **MISD (Multiple Instruction Stream, Single Data Stream)**: Wiele instrukcji operujących na jednym strumieniu danych.
- **MIMD (Multiple Instruction Stream, Multiple Data Stream)**: Wiele instrukcji operujących na wielu strumieniach danych.

## Architektura Systemów Równoległych

### Symetryczny Multiprocesor (SMP)

- **Właściwości**: Każdy procesor ma równy dostęp do pamięci.
- **Potencjalne zalety**: Zwiększona wydajność, łatwiejsze zarządzanie pamięcią.
- **Architektura**: Procesory współdzielą tę samą pamięć i magistrale.

### Procesor Wielordzeniowy

- **Procesor wielordzeniowy**: Procesor zawierający wiele rdzeni, z których każdy może wykonywać niezależne zadania.

### NUMA (Non-Uniform Memory Access)

- **NUMA**: Architektura pamięci, w której czas dostępu do pamięci zależy od lokalizacji pamięci względem procesora.

## Systemy Magistral

### Transakcje

- **Transakcje**: Operacje przesyłania danych pomiędzy różnymi komponentami systemu.

### Adresowanie Obiektów Przyłączonych do Magistrali

- **Typy adresowania**:
  - **Logiczne**: Adresowanie według logicznych identyfikatorów.
  - **Geograficzne**: Adresowanie według fizycznej lokalizacji.
  - **Zbiorowe**: Adresowanie grupy urządzeń jednocześnie.

### Protokół Magistral

- **Protokół magistral**: Zasady regulujące komunikację między urządzeniami przyłączonymi do magistrali.

### Synchroniczna i Asynchroniczna Realizacja Protokołu Magistrali

- **Synchroniczna**: Komunikacja zsynchronizowana z zegarem systemowym.
- **Asynchroniczna**: Komunikacja niezsynchronizowana z zegarem systemowym.

### Przesłania Niepowiązane

- **Zależności i problemy**: Problemy wynikające z braku synchronizacji między przesłaniami.

### Przesłania z Potwierdzeniem

- **Przesłania z potwierdzeniem**: Metoda zapewniająca, że przesłanie zostało odebrane poprawnie.

### AXI (Advanced eXtensible Interface)

- **AXI**: Standard interfejsu magistrali wysokiej wydajności używany w systemach wbudowanych.

### Arbitraż Magistrali

- **Statyczny**: Stała kolejność dostępu do magistrali.
- **Dynamiczny**: Kolejność dostępu do magistrali zmieniana dynamicznie w zależności od potrzeb.

### Problemy i Niezawodność Arbitrażu

- Problemy wynikające z konkurencji o dostęp do magistrali oraz techniki zapewniające niezawodność.

## Urządzenia Wejścia/Wyjścia (I/O)

### Sterowniki

- **Sterowniki**: Oprogramowanie umożliwiające komunikację między systemem operacyjnym a urządzeniami I/O.

### Oprogramowanie I/O

- Oprogramowanie zarządzające operacjami wejścia/wyjścia w systemie komputerowym.

### Procesy I/O

- **Klasyfikacja**: Różne typy procesów związanych z operacjami wejścia/wyjścia.

## Poufność i Bezpieczeństwo

### Aspekty Niezawodności

- **MTBF (Mean Time Between Failures)**: Średni czas między awariami.
- **MTTF (Mean Time To Failure)**: Średni czas do awarii.
- **Probability of Failure**: Prawdopodobieństwo wystąpienia awarii.
- **Niezawodność transmisji i przechowywania danych**: Techniki zapewniające niezawodność danych.

### Kody Detekcyjne i Korekcyjne

- **Kody detekcyjne**: Kody używane do wykrywania błędów w danych.
- **Kody korekcyjne**: Kody używane do korygowania błędów w danych.

### Macierze Dyskowe RAID

- **RAID (Redundant Array of Independent Disks)**: Technika zwiększająca niezawodność i wydajność dysków poprzez ich zorganizowanie w macierze.
