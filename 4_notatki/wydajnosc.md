# Wydajność

## Wydajność

### Pojęcia związane z wydajnością

- **Wydajność**: Miara efektywności przetwarzania przez system komputerowy.
- **Metryki wydajności**: Różne wskaźniki używane do oceny wydajności systemu.

### Metryki wydajności

- **Opóźnienie (latency)**: Czas od rozpoczęcia operacji do jej zakończenia.
- **Przepustowość (throughput)**: Ilość pracy wykonanej przez system w jednostce czasu.

## Czas Wykonania Programu

### Czas rzeczywisty / ścienny

- **Czas rzeczywisty (wall-clock time)**: Całkowity czas trwania wykonania programu, mierzony od momentu jego uruchomienia do zakończenia.

### Czas procesora

- **Czas procesora (CPU time)**: Czas, przez który procesor faktycznie pracuje nad wykonaniem programu.

### Narzędzia wysokopoziomowe / asembler

- **Narzędzia wysokopoziomowe**: Narzędzia do profilowania i analizy wydajności na poziomie kodu źródłowego.
- **Narzędzia asemblera**: Narzędzia do analizy i optymalizacji kodu maszynowego.

### RDTSC

- **RDTSC (Read Time-Stamp Counter)**: Instrukcja x86 do odczytu licznika czasu procesora.

### CPUID

- **CPUID**: Instrukcja x86 zwracająca informacje o procesorze, takie jak model, funkcje i konfiguracja.

### Wzory czasu

- **Wzory czasu**: Matematyczne wyrażenia używane do obliczania czasu wykonania programu na podstawie różnych czynników.

### Cykle, częstotliwości

- **Cykle**: Pojedyncze operacje zegara procesora.
- **Częstotliwość**: Liczba cykli na sekundę, mierzona w Hz.

### Moc, energia

- **Moc**: Ilość energii zużywanej przez procesor na jednostkę czasu, mierzona w watach (W).
- **Energia**: Całkowita ilość energii zużytej przez procesor podczas wykonania zadania, mierzona w dżulach (J).

### Przedrostki

- **Przedrostki**: Standardowe jednostki miary, takie jak kilo (k), mega (M), giga (G), tera (T), peta (P), eksa (E), zetta (Z), i jotta (Y).

### Pobór mocy

- **Pobór mocy**: Ilość mocy zużywanej przez system komputerowy lub jego komponenty.

### Liczba instrukcji

- **Liczba instrukcji (Instruction Count)**: Ilość instrukcji wykonywanych przez procesor.

### CPI

- **CPI (Cycles Per Instruction)**: Średnia liczba cykli zegara potrzebnych do wykonania jednej instrukcji.

### Pułapki

- **Pułapki**: Problemy i ograniczenia mogące wpłynąć na wydajność systemu.

### Parametry maszyny, moc obliczeniowa

- **Parametry maszyny**: Specyfikacje techniczne systemu komputerowego.
- **Moc obliczeniowa**: Zdolność systemu do wykonywania obliczeń.

### BLAS

- **BLAS (Basic Linear Algebra Subprograms)**: Biblioteka procedur wykorzystywanych w obliczeniach algebraicznych, często stosowana do testowania i optymalizacji wydajności.

### Intensywność arytmetyczna

- **Intensywność arytmetyczna**: Stosunek liczby operacji arytmetycznych do ilości przesyłanych danych.

### Model sufitowy

- **Model sufitowy**: Metoda analizy wydajności polegająca na określeniu maksymalnych możliwych osiągów systemu.

### Optymalizacja kodu: zasada Pareta

- **Zasada Pareta**: Reguła mówiąca, że 80% efektów pochodzi z 20% przyczyn; w kontekście wydajności oznacza to, że większość optymalizacji można osiągnąć poprzez poprawę niewielkiej liczby kluczowych fragmentów kodu.

### Przyspieszenie: Prawo Amdahla, Gustafsona-Barsisa

- **Prawo Amdahla**: Maksymalne przyspieszenie programu przy równoległym przetwarzaniu jest ograniczone przez sekwencyjną część programu.
- **Prawo Gustafsona-Barsisa**: Alternatywne podejście do oceny przyspieszenia, które uwzględnia zmienne obciążenia i wzrost liczby procesorów.

### Prawo Little'a

- **Prawo Little'a**: Formuła w teorii kolejek, która mówi, że średnia liczba klientów w systemie jest równa iloczynowi średniego czasu przebywania klienta w systemie i średniej liczby klientów wchodzących do systemu na jednostkę czasu.

### Techniki profilowania

- **Techniki profilowania**: Narzędzia i metody używane do analizy wydajności programu, identyfikacji wąskich gardeł i obszarów wymagających optymalizacji.

### Optymalizacje kompilatora

- **Optymalizacje kompilatora**: Techniki stosowane przez kompilatory w celu poprawy wydajności generowanego kodu maszynowego, takie jak eliminacja zbędnych instrukcji, rozwijanie pętli, optymalizacja dostępu do pamięci, itd.
