## Wymień poziomy równoległości drobnoziarnistej

Poziomy równoległości drobnoziarnistej obejmują:

1. **Instrukcyjną równoległość (Instruction Level Parallelism - ILP)**: równoczesne wykonywanie wielu instrukcji w jednym cyklu zegarowym.
2. **Równoległość wątków (Thread Level Parallelism - TLP)**: jednoczesne wykonywanie wielu wątków w ramach jednego procesu.
3. **Równoległość danych (Data Level Parallelism - DLP)**: równoczesne wykonywanie tej samej operacji na wielu elementach danych (np. SIMD - Single Instruction, Multiple Data).

## Wymień poziomy równoległości gruboziarnistej

Poziomy równoległości gruboziarnistej obejmują:

1. **Równoległość procesów (Process Level Parallelism)**: jednoczesne wykonywanie wielu niezależnych procesów.
2. **Równoległość aplikacji (Application Level Parallelism)**: wykonywanie różnych aplikacji równocześnie na różnych węzłach lub procesorach.
3. **Równoległość zadań (Task Level Parallelism)**: podział aplikacji na niezależne zadania, które mogą być wykonywane równolegle.

## Czym jest organizacja komputera? Podaj również jej założenia i cele

Organizacja komputera odnosi się do strukturalnych i operacyjnych właściwości komputera. Obejmuje konfigurację i interakcję między komponentami takimi jak procesory, pamięć, magistrale i urządzenia wejścia/wyjścia.

**Założenia i cele:**

1. **Optymalizacja wydajności**: poprawa czasu odpowiedzi i przepustowości.
2. **Efektywność energetyczna**: zmniejszenie zużycia energii przy zachowaniu wydajności.
3. **Skalowalność**: umożliwienie łatwej rozbudowy systemu.
4. **Modularność**: ułatwienie konserwacji i wymiany komponentów.
5. **Spójność**: zapewnienie, że komponenty mogą efektywnie współpracować.

## Przedstaw kolejne etapy w cyklu rozkazowym CISC

Cykl rozkazowy CISC (Complex Instruction Set Computing) obejmuje następujące etapy:

1. **Pobranie (Fetch)**: pobranie rozkazu z pamięci.
2. **Dekodowanie (Decode)**: dekodowanie rozkazu w celu ustalenia, jakie operacje należy wykonać.
3. **Pobranie operandów (Fetch Operands)**: pobranie danych, które będą używane przez rozkaz.
4. **Wykonanie (Execute)**: wykonanie operacji określonej przez rozkaz.
5. **Zapis wyników (Write Back)**: zapis wyników operacji do odpowiednich rejestrów lub pamięci.

## Przedstaw kolejne etapy w cyklu rozkazowym RISC

Cykl rozkazowy RISC (Reduced Instruction Set Computing) obejmuje następujące etapy:

1. **Pobranie (Fetch)**: pobranie rozkazu z pamięci.
2. **Dekodowanie (Decode)**: dekodowanie rozkazu.
3. **Pobranie operandów (Fetch Operands)**: pobranie danych potrzebnych do wykonania rozkazu.
4. **Wykonanie (Execute)**: wykonanie operacji.
5. **Zapis wyników (Write Back)**: zapis wyników operacji do odpowiednich rejestrów lub pamięci.

## Jak zorganizowany jest procesor sekwencyjny? Co go charakteryzuje?

Procesor sekwencyjny wykonuje instrukcje jedna po drugiej, bez jednoczesnego przetwarzania wielu instrukcji. Charakteryzuje się:

1. **Jednostką centralną (CU)**, która kontroluje wykonanie rozkazów.
2. **Jednostką arytmetyczno-logiczna (ALU)**, która wykonuje operacje arytmetyczne i logiczne.
3. **Rejestrami**, które przechowują dane i adresy.
4. **Pamięcią operacyjną (RAM)**, która przechowuje dane i rozkazy.
5. **Jednoliniowym przepływem danych**, co oznacza, że każda instrukcja musi zakończyć się przed rozpoczęciem następnej.

## Opisz krótko czym jest cykl rozkazowy

Cykl rozkazowy to seria kroków, które procesor wykonuje w celu pobrania, zdekodowania i wykonania instrukcji z pamięci. Składa się z etapów: pobranie (fetch), dekodowanie (decode), wykonanie (execute) i zapis wyników (write back).

## Z jakich modułów / jednostek składa się CPU?

CPU składa się z następujących modułów:

1. **Jednostka arytmetyczno-logiczna (ALU)**: wykonuje operacje arytmetyczne i logiczne.
2. **Jednostka sterująca (CU)**: kontroluje wykonanie instrukcji.
3. **Rejestry**: szybka pamięć do przechowywania danych i adresów.
4. **Cache**: pamięć podręczna dla szybszego dostępu do często używanych danych.
5. **Licznik rozkazów (PC - Program Counter)**: przechowuje adres następnej instrukcji do wykonania.
6. **Dekoder rozkazów**: interpretuje instrukcje.
7. **Jednostka zarządzania pamięcią (MMU)**: kontroluje dostęp do pamięci.

## Czym charakteryzuje się przetwarzanie potokowe?

Przetwarzanie potokowe (pipeline processing) charakteryzuje się podziałem wykonywania instrukcji na kilka etapów, które mogą być przetwarzane równocześnie. Pozwala to na zwiększenie przepustowości procesora i zmniejszenie opóźnień.

## Czym jest narzut separacji etapów w kontekście przetwarzania potokowego?

Narzut separacji etapów to dodatkowy czas i zasoby potrzebne do zarządzania i synchronizacji między różnymi etapami potoku. Może obejmować stany przejściowe, bufory i inne mechanizmy koordynacyjne, które zapewniają płynność przetwarzania.

## Wyjaśnij pojęcie kwantyzacji cyklu

Kwantyzacja cyklu to proces dzielenia cyklu zegarowego na mniejsze jednostki czasu, które mogą być wykorzystywane do równoczesnego przetwarzania różnych etapów instrukcji w potoku. Pozwala to na precyzyjne kontrolowanie przepływu danych i synchronizacji między etapami.

## Przedstaw kolejne etapy w przetwarzaniu potokowym

Kolejne etapy w przetwarzaniu potokowym to:

1. **Pobranie (Fetch)**: pobranie instrukcji z pamięci.
2. **Dekodowanie (Decode)**: dekodowanie instrukcji.
3. **Pobranie operandów (Fetch Operands)**: pobranie danych potrzebnych do wykonania instrukcji.
4. **Wykonanie (Execute)**: wykonanie operacji.
5. **Zapis wyników (Write Back)**: zapis wyników operacji do rejestrów lub pamięci.

## Czym są układy wykonawcze?

Układy wykonawcze (execution units) to komponenty CPU odpowiedzialne za wykonywanie instrukcji. Obejmują jednostki arytmetyczno-logiczne (ALU), jednostki zmiennoprzecinkowe (FPU), jednostki wektorowe oraz specjalizowane układy do przetwarzania grafiki lub kryptografii.

## Do czego służy i jak działa licznik rozkazów?

Licznik rozkazów (Program Counter, PC) przechowuje adres następnej instrukcji do wykonania. Zwiększa się automatycznie po pobraniu każdej instrukcji, a może być modyfikowany przez instrukcje skoku i wywołania procedur.

## Kiedy konieczny jest jednoczesny dostęp?

Jednoczesny dostęp jest konieczny, gdy wiele jednostek przetwarzających musi równocześnie odczytywać lub zapisywać dane do wspólnej pamięci lub rejestrów. Jest to typowe w systemach wieloprocesorowych, potokowych i superskalarnych.

## Czym jest procesor potokowy i jak jest zorganizowany?

Procesor potokowy jest zorganizowany w taki sposób, że wykonywanie instrukcji jest podzielone na kilka etapów, które są realizowane równocześnie przez różne segmenty procesora. Każdy segment realizuje inny etap instrukcji, co zwiększa przepustowość i efektywność przetwarzania.

## Zestaw ze sobą potok statyczny z dynamicznym

- **Potok statyczny**: Każda instrukcja przechodzi przez stałą, określoną liczbę etapów. Harmonogramowanie jest stałe i niezmienne.

- **Potok dynamiczny**: Liczba etapów i kolejność wykonania mogą się zmieniać w zależności od typu instrukcji i dostępnych zasobów. Jest bardziej elastyczny i lepiej przystosowuje się do różnych obciążeń.

## Jak wygląda przepływ danych w potoku? (co się dzieje w kolejnych cyklach)

Przepływ danych w potoku wygląda następująco:

1. **Fetch**: pobranie instrukcji z pamięci.
2. **Decode**: dekodowanie instrukcji i określenie wymaganych operacji.
3. **Fetch Operands**: pobranie danych potrzebnych do wykonania instrukcji.
4. **Execute**: wykonanie operacji arytmetycznych lub logicznych.
5. **Write Back**: zapis wyników operacji do rejestrów lub pamięci.

W każdym cyklu zegarowym, każda z tych operacji jest wykonywana równocześnie dla różnych instrukcji w potoku.

## Wyjaśnij czym jest potok płytki i głęboki?

- **Potok płytki**: ma mniejszą liczbę etapów, co może prowadzić do mniejszej przepustowości, ale prostszej organizacji i mniejszych opóźnień w pojedynczych etapach.
- **Potok głęboki**: ma więcej etapów, co zwiększa przepustowość, ale może zwiększać opóźnienia w razie wystąpienia konfliktów przetwarzania i wymaga bardziej skomplikowanego zarządzania.

## Wyjaśnij czym jest potok statyczny i dynamiczny?

- **Potok statyczny**: ma stałą liczbę i kolejność etapów, które każda instrukcja musi przejść. Harmonogramowanie jest stałe.
- **Potok dynamiczny**: etapy mogą się zmieniać w zależności od instrukcji i dostępnych zasobów. Harmonogramowanie jest elastyczne i dostosowuje się do różnych warunków.

## Przedstaw czynniki wpływające na czas wykonania poszczególnych etapów w cyklu rozkazowym

Czynniki wpływające na czas wykonania poszczególnych etapów to:

- **Złożoność instrukcji**: bardziej złożone instrukcje wymagają więcej czasu.
- **Szybkość pamięci**: czas dostępu do pamięci może wpłynąć na etapy pobierania i zapisu.
- **Przepustowość magistrali**: ograniczenia przepustowości mogą wpłynąć na szybkość przesyłania danych.
- **Konflikty zasobów**: rywalizacja o zasoby między różnymi jednostkami przetwarzającymi.
- **Architektura procesora**: różne architektury mają różne optymalizacje wpływające na czas wykonania.

## Przedstaw analizę SWOT dla CISC

**Strengths (Mocne strony):**

- Bogaty zestaw instrukcji umożliwia realizację skomplikowanych operacji w jednym rozkazie.
- Uproszczenie programowania poprzez bardziej abstrakcyjne instrukcje.

**Weaknesses (Słabe strony):**

- Złożona dekodowanie instrukcji może spowalniać procesor.
- Większe zużycie energii ze względu na bardziej skomplikowane układy.

**Opportunities (Szanse):**

- Może lepiej obsługiwać starsze programy i oprogramowanie wymagające specjalistycznych instrukcji.
- Może zyskać na znaczeniu w specyficznych zastosowaniach, gdzie złożone instrukcje są korzystne.

**Threats (Zagrożenia):**

- RISC zyskuje na popularności ze względu na prostotę i efektywność.
- Większa konkurencja ze strony nowoczesnych architektur procesorów.

## Przedstaw analizę SWOT dla RISC

**Strengths (Mocne strony):**

- Prosta i szybka dekodowanie instrukcji.
- Mniejsze zużycie energii dzięki prostocie układów.

**Weaknesses (Słabe strony):**

- Większa liczba instrukcji może być potrzebna do wykonania skomplikowanych zadań.
- Potrzeba bardziej zaawansowanego kompilatora, aby efektywnie wykorzystywać zestaw instrukcji.

**Opportunities (Szanse):**

- Wzrost popularności urządzeń mobilnych, gdzie liczy się efektywność energetyczna.
- Rozwój w obszarach serwerów i centrów danych, gdzie wydajność jest kluczowa.

**Threats (Zagrożenia):**

- Potencjalna konkurencja ze strony nowych architektur i technologii przetwarzania.
- Możliwe ograniczenia w obsłudze bardzo specjalistycznych aplikacji.

## Wytłumacz przejście z CISC do RISC

Przejście z CISC do RISC było motywowane potrzebą zwiększenia wydajności i zmniejszenia złożoności układów procesorów. RISC zredukowało liczbę i złożoność instrukcji, co uprościło dekodowanie i wykonanie rozkazów, pozwalając na większą wydajność i efektywność energetyczną. Dzięki temu możliwe stało się zastosowanie bardziej zaawansowanych technik optymalizacji, takich jak potokowanie i superskalowanie.

## Czym charakteryzują się przetwarzania potokowe / superskalarne / superpotokowe?

- **Przetwarzanie potokowe (Pipeline Processing)**: podział wykonywania instrukcji na kilka etapów, które są przetwarzane równocześnie.
- **Superskalarne przetwarzanie**: jednoczesne wykonywanie wielu instrukcji na różnych jednostkach wykonawczych w jednym cyklu zegarowym.
- **Superpotokowe przetwarzanie**: zwiększenie liczby etapów w potoku, co pozwala na jeszcze większą równoczesność przetwarzania i zwiększenie przepustowości.

## Jakie są możliwe przyczyny blokady potoku? (konflikty przetwarzania)

Możliwe przyczyny blokady potoku to:

- **Konflikty danych**: zależności między danymi, które muszą być spełnione przed wykonaniem kolejnej instrukcji.
- **Konflikty strukturalne (zasobu)**: brak dostępnych zasobów (np. jednostki wykonawczej, pamięci).
- **Konflikty sterowania**: zmiany w przepływie programu, takie jak skoki i rozgałęzienia, które mogą powodować przerwania w potoku.

## Przedstaw krótko konflikt danych, strukturalny (zasobu) oraz sterowania

- **Konflikt danych**: występuje, gdy instrukcje zależą od wyników poprzednich instrukcji, które nie zostały jeszcze zakończone.
- **Konflikt strukturalny (zasobu)**: występuje, gdy brakuje zasobów potrzebnych do wykonania instrukcji, np. dostępnej jednostki wykonawczej.
- **Konflikt sterowania**: występuje, gdy występują zmiany w przepływie programu (np. skoki), co powoduje, że potok musi być przerwany i zrestartowany.

## Jakie są skutki powyższych konfliktów przetwarzania?

Skutki konfliktów przetwarzania to:

- **Zmniejszenie przepustowości**: zmniejszona liczba instrukcji wykonywanych w jednostce czasu.
- **Zwiększone opóźnienia**: czas potrzebny na wykonanie pojedynczej instrukcji wzrasta.
- **Narzut zarządzania**: dodatkowe zasoby i mechanizmy potrzebne do zarządzania konfliktami.

## Przedstaw rodzaje potoków dynamicznych (I, II, III)

Rodzaje potoków dynamicznych obejmują:

- **Rodzaj I**: podstawowy potok dynamiczny z elastycznym harmonogramowaniem instrukcji.
- **Rodzaj II**: zaawansowane potoki dynamiczne z technikami spekulacyjnymi i predykcją rozgałęzień.
- **Rodzaj III**: najwyższy poziom zaawansowania, z pełnym wykorzystaniem zasobów, spekulatywnym wykonaniem i zaawansowaną predykcją rozgałęzień.

## Wyjaśnij pojęcie skoku opóźnionego

Skok opóźniony (delayed branch) to technika, w której instrukcja skoku nie jest wykonywana natychmiast, lecz po wykonaniu jednej lub więcej instrukcji, które następują po niej w kodzie programu. Pomaga to w minimalizowaniu opóźnień w potoku wynikających ze zmian przepływu sterowania.

## Wymień sposoby załagodzenia konfliktów przetwarzania

Sposoby załagodzenia konfliktów przetwarzania obejmują:

- **Reorganizacja kodu**: zmiana kolejności instrukcji w celu zmniejszenia zależności danych

.

- **Użycie rejestrów tymczasowych**: przechowywanie wyników pośrednich w rejestrach.
- **Spekulatywne wykonanie**: przewidywanie wyników i wykonywanie instrukcji przed ich rzeczywistym wystąpieniem.
- **Predykcja rozgałęzień**: przewidywanie kierunku skoku w celu minimalizacji opóźnień sterowania.

## Wytłumacz pojęcie statycznej oraz dynamicznej prognozy rozgałęzień

- **Statyczna prognoza rozgałęzień**: decyzje o przewidywaniu kierunku skoku są podejmowane na podstawie ustalonych reguł (np. zawsze skok do przodu).
- **Dynamiczna prognoza rozgałęzień**: decyzje są podejmowane na podstawie analizy historii wykonywania skoków i aktualnych warunków.

## Omów krótko bufor prognozy rozgałęzień

Bufor prognozy rozgałęzień (Branch Prediction Buffer) przechowuje historię poprzednich skoków i ich wyników, co pozwala na przewidywanie przyszłych skoków i minimalizowanie opóźnień związanych z konfliktem sterowania.

## Wyjaśnij czym jest prognoza rozgałęzień łączna

Prognoza rozgałęzień łączna (hybrid branch prediction) łączy różne metody prognozowania skoków, takie jak statyczna i dynamiczna, w celu poprawienia dokładności i minimalizacji opóźnień. Wykorzystuje zarówno ustalone reguły, jak i historyczne dane do przewidywania kierunku skoku.

## Wyjaśnij koncepcję wielomagistralowego dostępu do pliku rejestrowego

Koncepcja wielomagistralowego dostępu do pliku rejestrowego polega na umożliwieniu równoczesnego odczytu i zapisu wielu rejestrów, co pozwala na zwiększenie równoległości operacji i poprawę wydajności procesora.

## Wyjaśnij ideę niekolejnego wykonania rozkazu (zmiany kolejności rozkazów programu)

Nie kolejne wykonanie rozkazu (out-of-order execution) polega na wykonywaniu instrukcji nie w kolejności ich pojawiania się w programie, ale w kolejności dostępności danych i zasobów, co pozwala na bardziej efektywne wykorzystanie zasobów procesora i zwiększenie wydajności.

## Wyjaśnij jak dochodzi do zmiany kolejności wykonania rozkazów (schemat)

Zmiana kolejności wykonania rozkazów następuje w kilku krokach:

1. **Pobranie instrukcji**: instrukcje są pobierane z pamięci w kolejności ich występowania.
2. **Dekodowanie**: dekodowanie instrukcji w celu ustalenia ich operacji.
3. **Analiza zależności**: analiza zależności między instrukcjami i identyfikacja tych, które mogą być wykonane równocześnie.
4. **Harmonogramowanie**: ustalanie kolejności wykonania instrukcji na podstawie dostępności danych i zasobów.
5. **Wykonanie**: instrukcje są wykonywane w zmienionej kolejności.
6. **Zapis wyników**: wyniki są zapisywane w odpowiedniej kolejności, aby zapewnić zgodność z oryginalnym przepływem programu.

## Wyjaśnij do czego służy i na czym polega algorytm Tomasulo

Algorytm Tomasulo służy do dynamicznego harmonogramowania instrukcji i zarządzania zależnościami danych w procesorach. Polega na użyciu tablic rezerwacyjnych i mechanizmu spekulacji, aby umożliwić niekolejnościowe wykonanie instrukcji i minimalizować opóźnienia wynikające z zależności danych.

## Przedstaw z czego się składa algorytm Tomasulo

Algorytm Tomasulo składa się z:

- **Tablic rezerwacyjnych**: przechowują instrukcje i ich operandy, czekające na wykonanie.
- **Tablicy wyników**: przechowuje tymczasowe wyniki instrukcji do momentu ich zapisania.
- **Mechanizmu spekulacyjnego**: przewiduje wyniki operacji i wykonuje je przed ich faktycznym zatwierdzeniem.

## Wymień kolejne etapy algorytmu Tomasulo

Etapy algorytmu Tomasulo to:

1. **Pobranie instrukcji**: pobranie i umieszczenie instrukcji w tablicach rezerwacyjnych.
2. **Dekodowanie instrukcji**: dekodowanie i identyfikacja operandów.
3. **Sprawdzanie zależności**: sprawdzanie zależności danych i ustalanie kolejności wykonania.
4. **Wykonanie**: wykonanie instrukcji, gdy wszystkie operandy są dostępne.
5. **Zapis wyników**: zapis wyników w tablicy wyników i aktualizacja rejestrów.

## Przedstaw wady i zalety algorytmu Tomasulo

**Zalety:**

- Umożliwia niekolejnościowe wykonanie instrukcji, zwiększając wydajność.
- Skutecznie zarządza zależnościami danych, minimalizując opóźnienia.

**Wady:**

- Wymaga skomplikowanego sprzętu i zasobów do zarządzania tablicami rezerwacyjnymi.
- Może powodować dodatkowy narzut związany z spekulacją i zarządzaniem wynikami.

## Wyjaśnij pojęcie przetwarzania wektorowego

Przetwarzanie wektorowe polega na wykonywaniu operacji na całych wektorach danych jednocześnie, zamiast na pojedynczych elementach, co pozwala na znaczne przyspieszenie obliczeń matematycznych i naukowych.

## Wyjaśnij czym charakteryzuje się przetwarzanie wektorowe oraz jakie rozszerzenia wykorzystuje?

Przetwarzanie wektorowe charakteryzuje się jednoczesnym wykonywaniem operacji na zestawach danych, co zwiększa efektywność i wydajność obliczeń. Wykorzystuje rozszerzenia takie jak SIMD (Single Instruction, Multiple Data), SSE (Streaming SIMD Extensions) i AVX (Advanced Vector Extensions), które pozwalają na wykonywanie wielu operacji równocześnie.

## Wyjaśnij czym jest SSE

SSE (Streaming SIMD Extensions) to zestaw rozszerzeń instrukcji procesora, wprowadzony przez firmę Intel, który umożliwia przetwarzanie wektorowe. SSE pozwala na wykonywanie tej samej operacji na wielu danych jednocześnie, co zwiększa wydajność obliczeń w aplikacjach multimedialnych, naukowych i inżynierskich.
