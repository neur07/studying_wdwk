# Pamięć

## Wytłumacz pojęcie "Memory bottleneck" oraz jak wpływa na procesor

Memory bottleneck to zjawisko, w którym przepustowość pamięci ogranicza szybkość przetwarzania, co skutkuje wytworzeniem dodatkowych cykli oczekiwania (wait cycles) przez procesor. Procesor musi czekać na dane z pamięci, co spowalnia jego działanie i zmniejsza ogólną wydajność systemu.

## Wymień klasy pamięci ze względu na sposób dostępu do danych

- RAM (Random Access Memory)
- SAM (Sequential Access Memory)
- CAM (Content-addressable Memory)

## Wyjaśnij krótko sposób działania pamięci DDR(x)

Pamięć DDR (Double Data Rate) działa na zasadzie przesyłania danych dwukrotnie w każdym cyklu zegara. Oznacza to, że dane są przesyłane zarówno przy narastającym, jak i opadającym zboczu sygnału zegarowego, co skutkuje podwojeniem efektywnej przepustowości w porównaniu do tradycyjnej pamięci SDR (Single Data Rate).

## Przedstaw klasy pamięci ze względu na jej trwałość

Pamięć nieulotna (NVM):

- ROM
- NVRAM
- Flash Memory

Pamięć ulotna:

- statyczna SRAM
- dynamiczna DRAM

## Wymień przykłady DRAM

DRAM:

- z utrzymaniem wyjść EDO
- synchroniczne SDRAM
- podwójnej szybkości (DDR ... DDR4)
- pseudo-dwuportowe GDDR5

## Przedstaw kolejne kroki odczytu sekwencyjnego DAM (Direct Access Memory)

dane z nośnika sekwencyjnego -> bufor SIPO -> odczyt równoległy
blok danych -> bufor PISO -> zapis sekwencyjny

## Wymień różnice między DRAM a SRAM

DRAM:

- Napięcie na kondensatorze
- 1 tranzystor / bit
- mniejszy pobór mocy (tylko podczas odświeżania)
- wymaga regularnego odświeżania

SRAM:

- 4-6 tranzystorów / bit
- większy pobór mocy (stale załączona para tranzystorów)
- nie wymaga odświeżania

## Ile cykli potrzebuje pamięć RAM przy odczycie / zapisie

Odczyt - 2
Zapis - 1

## Wyjaśnij pojęcie ataku młotkowego

Atak młotkowy (row hammer) polega na wielokrotnym, szybkim przełączaniu stanu sąsiednich komórek pamięci (bitów), co może spowodować zmiany stanu bitów w pobliskich komórkach pamięci. W wyniku tego ataku może dojść do nieoczekiwanej zmiany danych, co jest wykorzystywane jako forma ataku na integralność danych w pamięci.

## Wyjaśnij pojęcie "Bank grouping"

Bank grouping to technika organizacji pamięci, która polega na podziale pamięci na grupy banków. Każda grupa banków może być dostępna niezależnie, co zwiększa równoległość i efektywność dostępu do pamięci. Dzięki bank grouping możliwe jest zredukowanie opóźnień wynikających z kolizji dostępu do różnych części pamięci.

## Activate, Read, Write

- **Activate**: Operacja aktywacji wiersza w pamięci DRAM. Procesor wysyła sygnał aktywacji do określonego wiersza, co powoduje jego przeniesienie do bufora wewnętrznego.
- **Read**: Operacja odczytu danych z aktywowanego wiersza. Dane są przenoszone z bufora wewnętrznego do procesora.
- **Write**: Operacja zapisu danych do aktywowanego wiersza. Procesor przesyła dane do bufora wewnętrznego, a następnie do określonego wiersza pamięci.

## Jak definiowana jest przepustowość pamięci? (Krótko opisz symbole)

Przepustowość pamięci jest definiowana jako ilość danych, która może być przesłana w określonym czasie. Wyrażana jest w jednostkach takich jak MB/s lub GB/s.

Wzór na przepustowość pamięci:
\[ B = w \times f \times c \]
gdzie:

- \( B \) - przepustowość pamięci (Bandwidth)
- \( w \) - szerokość magistrali danych (Data Bus Width)
- \( f \) - częstotliwość taktowania pamięci (Memory Clock Frequency)
- \( c \) - liczba transferów na cykl zegara (Transfers per Clock Cycle)

## Czym jest kanał w kontekście pamięci?

Kanał w kontekście pamięci odnosi się do niezależnej ścieżki komunikacji między kontrolerem pamięci a modułami pamięci. Każdy kanał może działać równolegle, co zwiększa ogólną przepustowość systemu pamięci.

## Na czym polega metoda kafelkowania?

Kafelkowanie polega na przetwarzaniu danych w małych, prostokątnych fragmentach (kafelkach) zamiast wierszach lub kolumnach, aby zwiększyć lokalność danych. W kontekście mnożenia macierzy, kafelkowanie pozwala na efektywniejsze wykorzystanie pamięci podręcznej, ponieważ przetwarzane są fragmenty danych, które znajdują się blisko siebie w pamięci.

## Wyjaśnij skróty RAS i CAS

- **RAS (Row Address Strobe)**: Sygnał używany do określenia wiersza w pamięci DRAM, który ma zostać aktywowany.
- **CAS (Column Address Strobe)**: Sygnał używany do określenia kolumny w pamięci DRAM, która ma zostać odczytana lub zapisana po aktywacji wiersza przez RAS.

## Wyjaśnij jak przebiega proces aktywacji i dezaktywacji wiersza przy odczycie danych z pamięci

1. **Aktywacja wiersza**: Procesor wysyła sygnał RAS do pamięci DRAM, co powoduje aktywację określonego wiersza. Dane z tego wiersza są ładowane do bufora wewnętrznego.
2. **Odczyt danych**: Po aktywacji wiersza procesor wysyła sygnał CAS, aby określić kolumnę, z której dane mają być odczytane. Dane z wybranej kolumny są przesyłane z bufora do procesora.
3. **Dezaktywacja wiersza**: Po zakończeniu odczytu, procesor wysyła sygnał do pamięci, aby dezaktywować wiersz i zwolnić bufor do kolejnych operacji.

## Wymień i krótko opisz parametry czasowe pamięci

- **CAS Latency (CL)**: Czas, jaki upływa od momentu wysłania sygnału CAS do momentu, gdy dane są dostępne na wyjściu.
- **RAS to CAS Delay (tRCD)**: Czas potrzebny na przejście od aktywacji wiersza (RAS) do aktywacji kolumny (CAS).
- **Row Precharge Time (tRP)**: Czas potrzebny na dezaktywację bieżącego wiersza przed aktywacją nowego wiersza.
- **Row Cycle Time (tRC)**: Czas potrzebny na zakończenie pełnego cyklu od aktywacji wiersza do jego dezaktywacji.

## Przedstaw czym jest transakcja blokowa

Transakcja blokowa polega na przesyłaniu dużych bloków danych w jednej operacji, zamiast przesyłania danych w małych, pojedynczych jednostkach. Jest to efektywny sposób przesyłania danych, który minimalizuje narzut związany z kontrolą transferu i maksymalizuje przepustowość.

## Przedstaw krótko proces mapowania adresu fizycznego

Proces mapowania adresu fizycznego polega na przekształceniu logicznego adresu, używanego przez program, na rzeczywisty adres w pamięci fizycznej. Mapowanie to jest zarządzane przez jednostkę zarządzania pamięcią (MMU) i tabelę stron (page table), która przechowuje informacje o odwzorowaniu adresów logicznych na fizyczne.

## Przedstaw krótko ideę DMA

DMA (Direct Memory Access) to technika umożliwiająca bezpośredni transfer danych między pamięcią a urządzeniami peryferyjnymi bez angażowania procesora. DMA pozwala na efektywne przesyłanie dużych ilości danych, ponieważ procesor nie musi wykonywać operacji I/O, co zwiększa ogólną wydajność systemu.

## Wymień oraz krótko opisz tryby pracy DMA

- **Blokowy (Burst Mode)**: DMA przejmuje kontrolę nad magistralą i przesyła cały blok danych w jednej operacji, blokując dostęp innych urządzeń do magistrali.
- **Podkradanie cykli (Cycle Stealing Mode)**: DMA przejmuje magistralę na krótki czas, wykonując małe transfery danych, co pozwala procesorowi na kontynuowanie pracy między transferami.
- **Przezroczysty (Transparent/Hidden Mode)**: DMA wykonuje transfery tylko wtedy, gdy magistrala jest nieużywana przez procesor, co minimalizuje wpływ na wydajność systemu.

## Wyjaśnij pojęcie transferu

Transfer w kontekście pamięci odnosi się do procesu przesyłania danych między różnymi elementami systemu komputerowego, takimi jak procesor, pamięć, urządzenia peryferyjne itp. Transfery mogą odbywać się za pomocą różnych mechanizmów, takich jak DMA, magistrale systemowe, interfejsy I/O itp. Celem transferu jest efektywne i szybkie przemieszczanie danych w systemie komputerowym.
