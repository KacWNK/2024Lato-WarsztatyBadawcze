# Wieloręki bandyta

**Zadanie warte 5 pkt**

## Osoba zgłoszona:

(a) Miłosz Kita

(b) ...

(c) ...

(d) ...

(e) ...

(f) ...

(g) ...

## Problem wielorękiego bandyty
Na zajęciach rozważaliśmy zadanie wielorękiego bandyty:

Mamy wiele maszyn, z których każde ma pewną nieznaną funkcję nagrody. "Granie" polega na wyborze maszyny, od której nagrodę otrzymamy. Celem jest granie tak, aby zdobyć sumarycznie jak największą nagrodę.

## Eksploracja kontra eksploatacja

Aby zdobyć dużą nagrodę, agent chciałby grać często na maszynie, która do tej pory się sprawdzała. Powinien jednak czasem grać na tych mniej obiecujących, bo być może okażą się one lepsze.

## UCB

Są argumenty teoretycznie oraz praktyczne przemawiająca za tym, że UCB jest najlepszym rozwiązaniem problemu wielorękiego bandyty. Niestety, słabo się ono uogólnia do pozostałych problemów RL.

UCB polega na wybraniu maszyny $a$, która maksymalizuje następującą wartość:

$Q_t(a) + c\sqrt{\frac{ln(t)}{N_t(a)}}$

gdzie $N_t(a)$ to liczba wyborów maszyny $a$.

## Zadanie
Zreprodukuj obrazek 2.4 ze strony 36 "Reinforcement Learning: An Introduction" Sutton, Barto. Czyli:

Estymuj wartość oczekiwaną bandyty jako średnią wartość z dotychczas wylosowanych wartości.

Porównaj 2 podejścia:

1. eps-greedy gdzie $\varepsilon = 0.1$
2. UCB, c=2

Narysuj wykres 2D, gdzie na osi OX będzie liczba gier, a na osi OY średnia zebrana nagroda.

### Wersja a
Mamy 10 bandytów:

1. $\mathcal{N}(1, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$

### Wersja b
Mamy 10 bandytów:

1. $\mathcal{N}(0.1, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$

### Wersja c
Mamy 10 bandytów:

1. $\mathcal{N}(0, 10)$
1. $\mathcal{N}(0, 10)$
1. $\mathcal{N}(0, 10)$
1. $\mathcal{N}(0, 10)$
1. $\mathcal{N}(0, 10)$
1. $\mathcal{N}(1, 0.1)$
1. $\mathcal{N}(1, 0.1)$
1. $\mathcal{N}(1, 0.1)$
1. $\mathcal{N}(1, 0.1)$
1. $\mathcal{N}(1.1, 0.1)$


### Wersja d
Mamy 10 bandytów:

1. Moduł z rozkładu Cauchy'ego minus 50, zwróć uwagę, że to ma nieskończoną wartość oczekiwaną
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$
1. $\mathcal{N}(0, 1)$


### Wersja e
Mamy 10 bandytów:

1. $U(0.1,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$
1. $U(0,1)$


### Wersja f
Mamy 10 bandytów:

1. $Exp(1)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$
1. $Exp(2)$


### Wersja g
Mamy 10 bandytów:

1. $Bernoulli(0.6)$, czyli 1 z p-stwem 0.6, 0 z p-stwem 0.4
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$
1. $Bernoulli(0.5)$







