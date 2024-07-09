# Stronicowanie i Segmentacja w architekturze x86

## Segmentacja

Segmentacja jest jednym ze sposobów zarządzania pamięcią w architekturze x86, który polega na dzieleniu przestrzeni adresowej na segmenty. Każdy segment ma określony rozmiar i bazę, co pozwala na bardziej elastyczne zarządzanie pamięcią.

- **Segmenty**: Fragmenty pamięci zdefiniowane przez bazę (adres początkowy) i limit (rozmiar). Mogą reprezentować różne części programu, takie jak kod, dane czy stos.

- **Deskryptory**: Struktury danych, które opisują segmenty. Zawierają informacje o bazie, limicie i prawach dostępu do segmentu.

- **Selekory**: Wskaźniki do deskryptorów segmentów. Są używane przez procesor do wybierania odpowiedniego deskryptora z tabeli deskryptorów.

W architekturze x86 istnieją dwie główne tabele deskryptorów:

- **GDT (Global Descriptor Table)**: Zawiera deskryptory dostępne dla całego systemu.
- **LDT (Local Descriptor Table)**: Zawiera deskryptory specyficzne dla konkretnego procesu.

## Stronicowanie

Stronicowanie jest mechanizmem zarządzania pamięcią, który dzieli przestrzeń adresową na strony (małe bloki o stałym rozmiarze). Umożliwia to efektywne mapowanie pamięci wirtualnej na fizyczną i izolację procesów.

- **Strony**: Jednostki pamięci o stałym rozmiarze (zwykle 4KB).

- **Tablice stron**: Struktury danych, które przechowują mapowania między stronami wirtualnymi a fizycznymi. W architekturze x86 z 32-bitową przestrzenią adresową istnieje wielopoziomowa hierarchia tablic stron:
  - **Page Directory (PD)**: Pierwszy poziom, który wskazuje na Page Table.
  - **Page Table (PT)**: Drugi poziom, który wskazuje na fizyczne ramki stron.

W architekturze x86_64 (64-bitowej), hierarchia jest rozszerzona do czterech poziomów:

- **PML4 (Page Map Level 4)**
- **PDPT (Page Directory Pointer Table)**
- **PD (Page Directory)**
- **PT (Page Table)**

# Bufory

Bufory to obszary pamięci używane do tymczasowego przechowywania danych, aby zminimalizować różnice w szybkości przetwarzania między różnymi komponentami systemu.

- **TLB (Translation Lookaside Buffer)**: Szybka pamięć podręczna, która przechowuje ostatnio używane mapowania stron wirtualnych na fizyczne. Zmniejsza liczbę bezpośrednich odwołań do tablic stron.

- **Cache**: Szybka pamięć podręczna, która przechowuje kopie często używanych danych z pamięci głównej. Występuje na kilku poziomach:
  - **L1 (Level 1)**: Najszybszy, najbliżej procesora, najmniejszy.
  - **L2 (Level 2)**: Wolniejszy od L1, większy.
  - **L3 (Level 3)**: Jeszcze wolniejszy, ale największy.

# Zorganizowanie pamięci wielopoziomowej

Pamięć wielopoziomowa w architekturze x86 jest zorganizowana w sposób hierarchiczny, aby zoptymalizować szybkość dostępu i efektywność zarządzania:

1. **Segmentacja**: Na najwyższym poziomie, przestrzeń adresowa jest dzielona na segmenty, które mogą obejmować różne obszary funkcjonalne programu (kod, dane, stos).

2. **Stronicowanie**: Wewnątrz segmentów, przestrzeń adresowa jest dalej dzielona na strony, które są mapowane na fizyczne ramki pamięci za pomocą wielopoziomowych tablic stron.

3. **Bufory i pamięć podręczna**: Aby przyspieszyć dostęp do danych, stosowane są różne poziomy pamięci podręcznej (L1, L2, L3) oraz TLB do przechowywania mapowań stron.

# Spójność działania

1. **CPU wykonuje instrukcję**: Procesor pobiera instrukcję, która zawiera adres wirtualny.
2. **Segmentacja**: Adres wirtualny jest przekształcany przez mechanizm segmentacji, który wykorzystuje selektory i deskryptory segmentów do określenia rzeczywistego adresu bazowego segmentu.
3. **Stronicowanie**: Otrzymany adres bazowy segmentu jest następnie poddany stronicowaniu. Procesor sprawdza w TLB, czy mapowanie strony jest już dostępne. Jeśli nie, odwołuje się do wielopoziomowych tablic stron, aby przetłumaczyć adres wirtualny na fizyczny.
4. **Bufory pamięci podręcznej**: Fizyczny adres jest następnie używany do dostępu do danych, które mogą być przechowywane w pamięci podręcznej (L1, L2, L3) lub w pamięci głównej, jeśli nie są dostępne w cache.

Dzięki temu wielopoziomowemu podejściu, system x86 osiąga równowagę między elastycznością zarządzania pamięcią a szybkością dostępu do danych.
