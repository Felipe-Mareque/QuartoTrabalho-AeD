# Trabalho – LeetCode 18: 4Sum

**Nome:** Felipe Reichow Mareque
**Turma:** M1

## Observação
NÃO CONSEGUI TERMINAR EM AULA

**A implementação foi desenvolvida utilizando como base o algoritmo de ordenação Merge Sort e a técnica de dois ponteiros.** O objetivo foi compreender a utilização de ordenação e busca eficiente para reduzir a quantidade de comparações necessárias na resolução do problema.

## Descrição

Este trabalho consiste na resolução do problema **LeetCode 18 – 4Sum**.

O problema fornece um vetor `nums` contendo números inteiros e um valor `target`. O objetivo é encontrar todas as quadruplas únicas:

```
[nums[a], nums[b], nums[c], nums[d]]
```

onde:

```
nums[a] + nums[b] + nums[c] + nums[d] == target
```

e os quatro índices utilizados devem ser distintos.

A resposta deve retornar todas as combinações possíveis sem repetições.

## Solução

Na solução foi utilizada inicialmente uma ordenação do vetor através do algoritmo **Merge Sort**.

Após o vetor estar ordenado, foi utilizada uma abordagem com dois laços de repetição para escolher os dois primeiros elementos da quadrupla e uma técnica de **dois ponteiros** para encontrar os outros dois elementos.

Os ponteiros utilizados funcionam da seguinte forma:

* `y` inicia após o segundo elemento escolhido e percorre o vetor aumentando seu valor quando a soma encontrada é menor que o objetivo.
* `z` inicia no final do vetor e diminui quando a soma encontrada é maior que o objetivo.

Como o vetor está ordenado, é possível ajustar os ponteiros sem precisar testar todas as combinações possíveis.

Também foram adicionadas verificações para evitar quadruplas duplicadas, ignorando valores repetidos durante a escolha dos elementos.

## Complexidade

* **Ordenação:** O(n log n), utilizando Merge Sort.
* **Busca das quadruplas:** O(n³).

Portanto, a complexidade total da solução é:

* **Tempo:** **O(n³)**.
* **Espaço:** **O(n)**.

O espaço é utilizado principalmente para armazenar as quadruplas encontradas e o vetor auxiliar utilizado pelo Merge Sort.
