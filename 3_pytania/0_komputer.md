# Komputer

## Czym jest program:

Wykład "WdWK - komputer.pdf" slajd 7

- Program = algorytm + struktury danych
- Program: sformalizowany opis sposobu wykonania działań
- Dane: symbole/znaki
- Sekwencja rozkazów zmieniających stan programu

## Wymień odpowiedniki między maszyną Turinga a komputerem:

Wykład "WdWK - komputer.pdf" slajd 10

- taśma - pamięć
- głowica - procesor
- stany maszyny - zawartość rejestrów procesora
- rozkazy maszyny - instrukcje procesora

## Wymień elementy komputera z programem przechowywanym:

Wykład "WdWK - komputer.pdf" slajd 11

- Procesor
- Magistrala
- Pamięć

## Czym się różni program od procesu i kodu pośredniego:

Wykład "WdWK - komputer.pdf" slajd 25

- Proces jest programem w trakcie wykonania: wiąże się z innymi procesami pamięci, występuje odwzorowanie kodu w przydzielonej pamięci, wyjątki
- Program jest opisem danych i działań (struktura danych, algorytm)
- Kod pośredni składa się z kodów operacyjnych, kodów danych, adresów danych w logicznej przestrzeni adresowej

## Czym są edycja, kompilacja, konsolidacja:

Wykład "WdWK - komputer.pdf" slajd 26

- Edycja - plik źródłowy
- Kompilacja - plik wynikowy
- Konsolidacja - tworzenie pliku wykonalnego

## Z czego się składa język asemblera:

Wykład "WdWK - komputer.pdf" slajd 33

- Mnemoniki instrukcji + argumenty
- Symbole, etykiety
- Wyrażenia
- Komentarze

## Wymień elementy modelu programowego procesora:

Wykład "WdWK - komputer.pdf" slajd 47

- lista rozkazów
- tryby adresowania
- rejestry
- typy danych
- obsługa wyjątków

## Jakie są klasyfikacje instrukcji:

Wykład "WdWK - komputer.pdf" slajd 49

- przesłania danych
- operacje logiczne
- zmiany formatu
- konwersje
- arytmetyka
- rozgałęzienia
- specjalne (nop, nea, cpuid)
- instrukcje koprocesorów
- systemowe

## Wymień tryby adresowania:

Wykład "WdWK - komputer.pdf" slajd 51

- Bezpośrednie - wartość lub adres:
  - zwarte (cpuid)
  - natychmiastowe ($100)
  - bezwzględne (inc 100)
  - bezpośrednie rejestrowe (inc %eax)
- Pośrednie (inc(%eax))

## Opisz model adresowania pamięci w x86:

Wykład "WdWK - komputer.pdf" slajd 52

- tryb adresowania - sposób obliczenia pamięci w logicznej przestrzeni adresowania;
- adres fizyczny - wynik przekształcenia adresu logicznego;
- pamięć segmentowana adres - segment: [baza + indeks * skala + przemieszczenie]
  - seg = cs, ds, es, fs, gs, ss;
  - baza/indeks = eax, ebx, ecx, edx, esi, edi, ebp, esp (baza != esp)
- adres: [baza + indeks * skala + przemieszczenie]
  - baza/indeks = dowolny rejestr 32- lub 64-bitowy (baza != esp/rsp)

## Opisz rozmiary rejestrów w x86:

Wykład "WdWK - komputer.pdf" slajd 54

- BPER:
  - [32/64-bits] General-Purpose Registers: eax, ebx, ecx, edx, esi, edi, ebp, esp
  - [16-bits] Segment Registers
  - [64-bits] RFLAGS Registers
  - [64-bits] RIP
- FPU Registers:
  - [80-bits] 8-Floating-point Data Registers
  - [16-bits] Control registers
  - [16-bits] Status Registers
  - [16-bits] Tag Registers
  - [64-bits] FPU IPR
  - [64-bits] FPU DPR
- SSE:
  - [64-bits] 8-MMX
  - [128-bits] 16 XMM

## Wymień typy danych:

Wykład "WdWK - komputer.pdf" slajd 56

- Podstawowe: bajt, słowo, podwójne/poczwórne słowo
- Liczbowe:
  - stałoprzecinkowe
  - zmiennoprzecinkowe
  - wektorowe
- Wskaźnikowe
- Pola bitowe
- Ciągi

## Wymień tryby adresowania argumentów instrukcji:

Wykład "WdWK - komputer.pdf" slajd 59

- natychmiastowe
- rejestry
- porty we/wy
- lokacje w pamięci

## Czym są bit, bajt, słowo:

Wykład "WdWK - komputer.pdf" slajd 68

- bajt - jednostka podstawowa
- słowo - jednostka logiczna organizacji programu

## Opisz z czego się składa instrukcja:

Inst. Pref. -> Opcode -> modR/M -> SIB -> Displacement -> Immediate

## Wymień rodzaje instrukcji:

Wykład "WdWK - komputer.pdf" slajd 74

- Przesłania danych (MOV, XCHG...)
- Operacje logiczne (NOT, NEG, OR...)
- Zmiana formatu (CWD, CDQ...)
- Operacje arytmetyczne (ADD, ADC, SUB, SBB...)
- Rozgałęzienia (JMP, CALL, RET...)

## Wymień elementy ramki stosu, podaj rejestry wywołujące funkcje:

Wykład "WdWK - komputer.pdf" slajd 110

- Lokalna struktura dynamiczna
- Wskaźnik struktury
- Chronione rejestry
- Adres powrotu
- Stan procesora
- Argumenty funkcji

Rejestry wywołujące: %ebp, %ebx, %edi, %esi, %esp

%eax - an integral or pointer

## Opisz powiązania instrukcji tworzące program

Wykład "WdWK - komputer.pdf" slajd 110

- sekwencyjne - bez sterowania
- łańcuchowe - umożliwia sterowanie

## Czym jest rozgałęzienie:

Wykład "WdWK - komputer.pdf" slajd 111

- Jest wyborem alternatywnej ścieżki przetwarzania

## Opisz główne cechy funkcji:

Wykład "WdWK - komputer.pdf" slajd 111

- przekazywanie argumentów
- blok aktywacji (kontekst)
- kapsułowanie
- zakończenie zwrotu wyniku

## Opisz mechanizm działania funkcji call:

Wykład "WdWK - komputer.pdf" slajd 133

- Zachowanie mechanizmu powrotu, czyli bieżący adres instrukcji w EIP, a następnie na stosie
- Przechodzenie do adresu docelowego
- EIP ustawia się na adres docelowej funkcji

## Czym jest ABI i co definiuje:

Wykład "WdWK - komputer.pdf" slajd 136

- To jest interfejs binarny aplikacji
- definiuje:
  - typy danych
  - sposób wywołania funkcji: przekazywanie parametrów, zwracanie wartości
  - sposób wywołania funkcji systemowych
  - formaty i nazwy plików bibliotecznych, nagłówkowych, programów

## Konwencje wywołania funkcji:

Wykład "WdWK - komputer.pdf" slajd 148

- Konwencja wywołania - sposób przekazywania parametrów z i do funkcji
- Proces przekazywania parametrów - powiązanie procedury
- Konwencje:
  - przez rejestry procesora
  - przez obszar powiązania danych
  - przez stos programowy

## Opisz wady i zalety funkcji:

Wykład "WdWK - komputer.pdf" slajd 149

- Wady:
  - Redukcja rozmiaru kodu
  - Redukcja zapotrzebowania na pamięć
  - Ukrycie szczegółów algorytmu
  - Łatwa implementacja poziomu abstrakcji
- Zalety:

  - Naruszenie sekwencyjności rozkazów podczas wykonania

  - Nieprzewidywalność lokalizacji kolejnego rozkazu podczas powrotu
