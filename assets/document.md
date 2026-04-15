# Cel ćwiczenia

Celem przeprowadzonego ćwiczenia było wykorzystanie
algorytmóœ automatycznej kontroli błędów oraz dynamicznego doboru kroku czasowego
na przykładzie metody Eulera oraz Rungego-Kutty 4 rzędu przy rozwiązywaniu równań
dynamiki Newtona.

# Wyniki pomiarów

## Kontrola Błędów

```{figure} ./ex2.png
Wykres położenia x(y) (góra) oraz y(t) (dół) dla metody Eulera
```

```{figure} ./ex3.png
Wykres położenia x(y) (góra) oraz y(t) (dół) dla metody RK4
```

jak widać, metoda Eulera wykazuje znaczne odchylenie (wzrost promienia okręgów) w porównaniu do metody RK4, która w miarę dobrze utrzymuje zadany kształt
dla ustalonego $\Delta t = 1000s$.

## Dynamiczny dobór kroku czasowego
Następnie, korzystająć z odpowiedniego algorytmu dobrano odpowiedni krok czasowy dla poszczególnych metod, tak, aby tolerancja mieściła się w zadanym przedziale.
Dla metody Eulera, gdy zadano tolerancję $10^3$, otrzymano następujące wyniki
$\Delta t=1350.8517176729927$

```{figure} ./ex5-1.png
Wykres położenia x(y) (góra) oraz y(t) (dół) dla metody Eulera z dynamicznym doborem kroku czasowego dla tolerancji zadanej na $10^3$
```

Natomiast dla mniejszej tolerancji (100m) otrzymano $\Delta t = 423.9115827521624$

```{figure} ./ex5-2.png
Wykres położenia x(y) (góra) oraz y(t) (dół) dla metody Eulera z dynamicznym doborem kroku czasowego dla tolerancji zadanej na $10^2$
```

Dla metody RK4 można było dobrać znacznie większe kroki czasowe co wpłynęło na znacznie krótszy czas wykonania kodu.
Dla tolerancji $1000m$ otrzemano $\Delta t = 478296.9s$.

```{figure} ./ex6-1.png
Wykres położenia x(y) (góra) oraz y(t) (dół) dla metody RK4 z dynamicznym doborem kroku czasowego dla tolerancji zadanej na $10^3$10
```

Natomiast dla mniejszej zadanej tolerancji (1m) otrzymano $\Delta t = 121576.65459056932s$
```{figure} ./ex6-2.png
Wykres położenia x(y) (góra) oraz y(t) (dół) dla metody RK4 z dynamicznym doborem kroku czasowego dla tolerancji zadanej na $10^0$
```

# Podsumowanie

Porównując obie metody symulacyjne, można zauważyć, że metoda RK4 jest znacznie lepsza,
niż metoda Eulera.
Porównując również czasy wykonania obu metod, można zauważyć, że pomimo że metoda RK4 jest bardziej złożona i trwa dłużej
przy unjormowanym kroku czasowym, jest ona również znacznie bardziej dokłądna, co pozwala na użycie dłuższego kroku czasowego.
W efekcie mimo swojej złożoności jest ona również szybsza.

# Literatura

- kod projektu https://github.com/gucio321-studies/MOFProj2 nr zmiany: 34891b9bcd4f766e45789e9bcef4a31e9561887a
