---
layout: post
title: "Tugas CaGaib: Model Hidden Markov"
date: 2017-05-27
---

Model Hidden Markov yang akan disingkat sebagai HMM merupakan sebuah pendekatan dengan model generatif. Model ini akan melakukan kalkukasi joint probability antara paired observation dengan sekuens label. Kemudian, dipilih parameter-parameter tertentu yang dapat memaksimalkan hasil dari joint probability.

Terdapat beberapa variabel yang berguna dalam penggunaan model Hidden Markov, diantaranya adalah sebagai berikut:
1. λ = (A, B, π), di mana A merepresentasikan transition probability dan B merepresentasikan emission probability dan π merepresentasikan start probability;
2. A = aij, di mana A merupakan variabel yang sama seperti pada nomor 1 dan merupakan banyaknya transisi yang terjadi dari state si ke sj;
3. B = bjk, di mana B merupakan variabel yang sama seperti pada nomor 1 dan merupakan lamanya waktu dari state sj ke sk.

Selain ketiga variabel tersebut, model ini juga memanfaatkan algoritma viterbi. Algoritma viterbi ditemukan oleh Viterbi pada tahun 1967 dan digunakan untuk mencari pattern dengan frekuensi pada distribusi tag-tag tertentu berdasarkan state transition probabilities. Algoritma ini dapat membantu HMM dalam menemukan tags yang optimal pada perhitungan linear. Ide yang digunakan adalah dengan terlebih dahulu memilih sekuens-sekuens yang paling memungkinkan. Untuk itu dibutuhkan beberapa parameter sebagai berikut:
1. Himpunan status, S;
2. Observasi, O/k;
3. Transition probability, A;
4. Emission probability, B;
5. State probabilities awal, π.
