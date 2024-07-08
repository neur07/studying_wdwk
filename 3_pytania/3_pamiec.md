# Pamięć

## Wytłumacz pojęcie "Memory bottleneck" oraz jak wpływa na procesor

Memory bottleneck to zjawisko w którym to przepustowość pamięci ogranicza szybkość przetwarzania, co skutkuje wytworzeniem dodatkowych cykli oczekiwania (wait cycles) przez procesora

## Wymień klasy pamięci ze względu na sposób dostępu do danych

- RAM (Random Access Memory)
- SAM (Sequential Access Memory)
- CAM (Content-addressable Memory)

## Wyjaśnij krótko sposób działania pamięci DDR(x)

## Przedstaw klasy pamięci ze względu na jej trwałość

Pamięć nieulotna (NVM):

- ROM
- NVRAM

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
blok danych ->bufor PISO -> zapis sekwencyjny

## Wymień różnice między DRAM a SRAM

DRAM:

- Napięcie na kondensatorze
- 1 tranzystor / bit
- mniejszy pobór mocy (tylko podczas odświeżania)

SRAM (CMOS / TTL):

- 4-6 tranzystorów / bit
- duży pobór mocy (stale załączona para tranzystorów)

## Ile cykli potrzebuje pamięć RAM przy odczycie / zapisie

Odczyt - 2
Zapis - 1

## Wyjaśnij pojęcie ataku młotowego

## Wyjaśnij pojęcie "Bank grouping"

## Activate, Read, Write ????

## Jak definiowana jest przepustowość pamięci? (Krótko opisz symbole)

$B = w \* $

## Czym jest kanał w kontekście pamięci?

## Wyjaśnij skróty RAS i CAS

## Wyjaśnij jak przebiega proces aktywacji i dezaktywacji wiersza przy odczycie danych z pamięci

## Wymień i krótko opisz parametry czasowe pamięci

## Przedstaw czym jest transakcja blokowa

## Przedstaw krótko proces mapowania adresu fizycznego

## Wymień oraz krótko opisz tryby pracy DMA

- blokowy (ang. burst mode) - pełna blokada magistrali pamięci podczas transferu DMA
- podkradanie cykli (ang. cycle stealing mode) - częste blokowanie magistrali na krótki czas
- przezroczysty (ang. transparent/hidden mode) - transfer DMA tylko gdy magistrala pamięci nie jest używana przez CPU

##
