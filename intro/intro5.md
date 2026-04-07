# Porównanie dwóch sekwencji: alignment i dot-plot

Porównywanie dwóch sekwencji biologicznych (DNA, RNA lub białek) jest jednym z podstawowych zadań bioinformatyki. Pozwala wykrywać podobieństwa i różnice między sekwencjami, co z kolei umożliwia przewidywanie ich funkcji oraz identyfikowanie mutacji i kluczowych regionów sekwencji o znaczeniu funkcjonalnym lub strukturalnym.

Wyróżnia się dwa podstawowe podejścia do porównywania sekwencji (opisane poniżej).

## 1. Przyrównanie (dopasowanie) sekwencji (*alignment*)

Przyrównanie dwóch sekwencji polega na ich ułożeniu względem siebie w taki sposób, aby uzyskać matematycznie najlepsze dopasowanie zgodnie z przyjętym schematem punktowania. Schemat ten określa wartości dla:
- zgodności (*match*),
- niezgodności (*mismatch*),
- przerw (*gaps*), odpowiadających insercjom lub delecjom.

Wyróżniamy dwa podstawowe typy dopasowań:

* **Przyrównanie globalne** – porównuje całe sekwencje od początku do końca, uzyskując najlepsze możliwe pełne przyrównanie (algorytm Needlemana–Wunscha).
* **Przyrównanie lokalne** – wyszukuje najlepiej dopasowane fragmenty w obrębie dwóch sekwencji (algorytm Smitha–Watermana).

Podstawową metodą obliczeniową wykorzystywaną w obu przypadkach jest **programowanie dynamiczne**, które pozwala szybko i dokładnie znaleźć optymalne dopasowanie poprzez:
- zbudowanie macierzy punktów dopasowania,
- wyznaczenie najlepszego dopasowania na podstawie tej macierzy,
- odtworzenie rozwiązania poprzez prześledzenie ścieżki wstecz (*traceback*).

## 2. Dot-plot

Dot-plot to graficzna metoda porównywania dwóch sekwencji, która pozwala wizualnie ocenić ich podobieństwo.

- oś wykresu odpowiada jedną sekwencję,
- punkt na wykresie oznacza dopasowanie fragmentów,
- przekątne wskazują regiony podobieństwa.

Dot-plot jest szczególnie przydatna do wykrywania:

- powtórzeń w sekwencjach,
- insercji i delecji,
- inwersji,
- regionów homologicznych między sekwencjami

## 3. Kluczowa różnica

- **Przyrównanie (alignment)** daje dokładny wynik znak po znaku sekwencji oraz jego liczbową punktację.
- **Dot-plot** daje szybki, wizualny obraz podobieństw i zmian strukturalnych.

Obie metody się uzupełniają i są szeroko stosowane w analizie sekwencji biologicznych.