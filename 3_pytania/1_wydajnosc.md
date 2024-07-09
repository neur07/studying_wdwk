## Wytłumacz krótko pojęcie wielobieżności

Wykład "WdWK - wydajnosc.pdf" slajd 2

---

Wielobieżność to zdolność systemu operacyjnego do jednoczesnego wykonywania wielu procesów lub wątków. Pozwala to na efektywniejsze wykorzystanie zasobów procesora poprzez równoczesne wykonywanie różnych zadań.

## Przedstaw krótko różne aspekty wydajności

Wykład "WdWK - wydajnosc.pdf" slajd 2

---

Wydajność systemu komputerowego można oceniać przez pryzmat kilku aspektów:

- **Przepustowość (throughput)**: liczba operacji wykonywanych w jednostce czasu.
- **Opóźnienie (latency)**: czas potrzebny do zakończenia pojedynczej operacji.
- **Utylizacja zasobów**: efektywne wykorzystanie dostępnych zasobów, takich jak CPU, pamięć, dysk.
- **Skalowalność**: zdolność systemu do zachowania wydajności w miarę wzrostu obciążenia lub liczby zasobów.

## Podaj i wyjaśnij wzór na czas wykonania programu

Wykład "WdWK - wydajnosc.pdf" slajd 11

---

Czas wykonania programu \( T \) można wyrazić wzorem:
\[ T = \frac{CPI \times Ni \times T\_{cyklu}}{f} \]
gdzie:

- \( CPI \) - średnia liczba cykli na instrukcję,
- \( Ni \) - liczba wykonanych instrukcji,
- \( T\_{cyklu} \) - czas trwania cyklu procesora,
- \( f \) - częstotliwość zegara procesora.

## Od czego zależy czas cyklu procesora

Wykład "WdWK - wydajnosc.pdf" slajd 12

---

Czas cyklu procesora zależy od technologii wykonania układów scalonych, ich architektury oraz napięcia zasilania. Krótszy czas cyklu oznacza szybszy procesor, ale wymaga lepszych technologii produkcji i może prowadzić do większego zużycia energii i większego wydzielania ciepła.

## Podaj i wyjaśnij wzór na moc / energię procesora

Wykład "WdWK - wydajnosc.pdf" slajd 13

---

Moc \( P \) procesora można wyrazić wzorem:
\[ P = C \times V^2 \times f \]
gdzie:

- \( C \) - pojemność ładunku przełączającego (capacitance),
- \( V \) - napięcie zasilania,
- \( f \) - częstotliwość zegara procesora.

Energia zużywana przez procesor jest iloczynem mocy i czasu działania.

## Podaj i wyjaśnij wzór na pobór mocy

Wykład "WdWK - wydajnosc.pdf" slajd 13

---

Pobór mocy \( P \) przez system komputerowy jest sumą mocy dynamicznej i mocy statycznej:
\[ P*{total} = P*{dynamic} + P\_{static} \]

Moc dynamiczna:
\[ P\_{dynamic} = C \times V^2 \times f \]

Moc statyczna wynika z prądów upływu i może być wyrażona jako:
\[ P*{static} = I*{leak} \times V \]
gdzie:

- \( I\_{leak} \) - prąd upływu.

## Zestaw ze sobą kilka odpowiadających sobie przedrostków dwójkowych z SI

Wykład "WdWK - wydajnosc.pdf" slajd 15

---

| SI       | Dwójkowy              |
| -------- | --------------------- |
| kilo (k) | kibibyte (KiB) - 2^10 |
| mega (M) | mebibyte (MiB) - 2^20 |
| giga (G) | gibibyte (GiB) - 2^30 |
| tera (T) | tebibyte (TiB) - 2^40 |

## Od czego zależy liczba wykonań instrukcji?

Wykład "WdWK - wydajnosc.pdf" slajd 22

---

Liczba wykonań instrukcji zależy od:

- złożoności algorytmu,
- efektywności kodu,
- liczby iteracji w pętlach oraz
- ilości wykonywanych operacji warunkowych.

## Od czego zależy średnia liczba cykli na instrukcję?

Wykład "WdWK - wydajnosc.pdf" slajd 23

---

Średnia liczba cykli na instrukcję (CPI) zależy od architektury procesora, optymalizacji pipeline’u, rozkładu typów instrukcji oraz efektywności cache’a i innych jednostek wykonawczych.

## Podaj i wyjaśnij wzór na przepustowość

Wykład "WdWK - wydajnosc.pdf" slajd 27

---

Przepustowość \( B \) systemu można wyrazić wzorem:
\[ B = \frac{I}{T} \]
gdzie:

- \( I \) - liczba operacji,
- \( T \) - czas.

## Zdefiniuj i wytłumacz od czego zależy moc obliczeniowa

Wykład "WdWK - wydajnosc.pdf" slajd 28

---

Moc obliczeniowa systemu to zdolność do wykonywania operacji w jednostce czasu, zwykle mierzona w FLOP/s (operacje zmiennoprzecinkowe na sekundę). Zależy od architektury procesora, liczby rdzeni, efektywności algorytmów oraz wydajności pamięci i innych podsystemów.

## Wytłumacz pojęcie zrównoważenia maszyny (machine balance)

Wykład "WdWK - wydajnosc.pdf" slajd 31

---

Zrównoważenie maszyny to proporcja między mocą obliczeniową a przepustowością pamięci. Optymalne zrównoważenie pozwala na maksymalne wykorzystanie zasobów bez wąskich gardeł.

## Czym jest FLOP?

Wykład "WdWK - wydajnosc.pdf"

---

FLOP (Floating Point Operation) to pojedyncza operacja arytmetyczna na liczbach zmiennoprzecinkowych, np. dodawanie, odejmowanie, mnożenie, dzielenie.

## Podaj i wyjaśnij wzór na intensywność arytmetyczną/operacyjną

Wykład "WdWK - wydajnosc.pdf" slajd 33

---

Intensywność arytmetyczna \( AI \) to liczba operacji arytmetycznych na jednostkę transferu danych:
\[ AI = \frac{FLOP}{D} \]
gdzie:

- \( FLOP \) - liczba operacji zmiennoprzecinkowych,
- \( D \) - ilość przesłanych danych.

## Wyjaśnij pojęcie modelu sufitowego oraz co reprezentują osie wykresu

Wykład "WdWK - wydajnosc.pdf" slajd 35

---

Model sufitowy (roofline model) przedstawia zależność między intensywnością arytmetyczną a wydajnością obliczeniową. Oś x reprezentuje intensywność arytmetyczną, a oś y maksymalną możliwą wydajność (FLOP/s). Model pokazuje, jak blisko teoretycznego maksimum znajduje się aktualna wydajność.

## Wyjaśnij czym jest region optymalizacji

Wykład "WdWK - wydajnosc.pdf" slajd 35

---

Region optymalizacji to obszar w wykresie modelu sufitowego, gdzie optymalizacja kodu może przynieść największe korzyści. Zwykle dotyczy to kodu znajdującego się poniżej "sufitu" pamięciowego lub obliczeniowego, gdzie istnieje potencjał na zwiększenie intensywności arytmetycznej lub przepustowości pamięci.

## O czym mówi zasada Pareta?

Wykład "WdWK - wydajnosc.pdf" slajd 41

---

Zasada Pareta (zasada 80/20) mówi, że 80% efektów pochodzi z 20% przyczyn. W kontekście optymalizacji, oznacza to, że większość problemów z wydajnością może być spowodowana przez niewielką część kodu.

## Krótko przedstaw Prawo Amdahla

Wykład "WdWK - wydajnosc.pdf" slajd 43

---

Prawo Amdahla opisuje potencjalne przyspieszenie programu przez równoległe przetwarzanie. Mówi, że maksymalne przyspieszenie jest ograniczone przez sekwencyjną część programu, której nie da się równolegle przetworzyć.

## Podaj i wyjaśnij wzór na przyspieszenie w Prawie Amdahla

Wykład "WdWK - wydajnosc.pdf" slajd 43

---

Przyspieszenie \( S \) według Prawa Amdahla wyraża się wzorem:
\[ S = \frac{1}{(1 - P) + \frac{P}{N}} \]
gdzie:

- \( P \) - procent programu, który można zrównoleglić,
- \( N \) - liczba procesorów.

## Krótko przedstaw Prawo Gustafsona

Wykład "WdWK - wydajnosc.pdf" slajd 46

---

Prawo Gustafsona proponuje, że zwiększając rozmiar problemu (a nie tylko liczbę procesorów), można osiągnąć lepsze przyspieszenie, ponieważ większa część programu może być równolegle przetworzona.

## Podaj i wyjaśnij wzór na przyspieszenie w Prawie Gustafsona

Wykład "WdWK - wydajnosc.pdf" slajd 46

---

Przyspieszenie \( S \) według Prawa Gustafsona wyraża się wzorem:
\[ S = N - (N - 1) \times (1 - P) \]
gdzie:

- \( N \) - liczba procesorów,
- \( P \) - procent programu, który można zrównoleglić.

## Czym jest skalowanie silne i słabe?

Wykład "WdWK - wydajnosc.pdf" slajd 49

---

- **Skalowanie silne**: wydajność systemu rośnie proporcjonalnie do liczby procesorów przy stałym rozmiarze problemu.
- **Skalowanie słabe**: wydajność systemu rośnie proporcjonalnie do liczby procesorów przy wzrastającym rozmiarze problemu.

## Wymień cele optymalizacji kodu

Wykład "WdWK - wydajnosc.pdf" slajd 51

---

- Zwiększenie wydajności (szybsze wykonanie).
- Zmniejszenie zużycia zasobów (pamięć, moc).
- Poprawa czytelności i utrzymywalności kodu.
- Redukcja liczby błędów.

## Krótko omów Prawo Little'a

Wykład "WdWK - wydajnosc.pdf" slajd 53

---

Prawo Little'a w teorii kolejek mówi, że średnia liczba klientów \( L \) w systemie jest równa średniemu współczynnikowi przyjścia klientów \( \lambda \) pomnożonemu przez średni czas spędzony w systemie \( W \):
\[ L = \lambda \times W \]

## Wymień przykładowe techniki profilowania

Wykład "WdWK - wydajnosc.pdf" slajd 56

---

- Analiza statyczna (analiza kodu bez uruchamiania).
- Analiza dynamiczna (śledzenie wykonania programu).
- Profilowanie czasu CPU (mierzenie czasu wykonania funkcji).
- Profilowanie pamięci (śledzenie alokacji i dealokacji pamięci).
- Profilowanie I/O (analiza operacji wejścia/wyjścia).
