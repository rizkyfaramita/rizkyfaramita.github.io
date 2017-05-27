---
layout: post
title: Tugas Artikel CaGaib: Pengenalan Entitas dengan Pendekatan Model Hidden Markov
date: 2017-05-27
---

Dalam menyelesaikan permasalah pengenalan entitas dengan menggunakan pendekatan dari model hidden Markov berikut adalah langkah-langkah yang secara berurutan dilakukan:
1. Menyiapkan data
2. Mengestimasi parameter HMM
3. Melakukan testing


Langkah 1: Menyiapkan Data
Data mentah yang pertama kali didapatkan perlu diproses terlebih dahulu agar data tersebut dapat digunakan sebagai parameter-parameter pada HMM. Training yang dilakukan untuk mengubah data mentah tersebut menjadi data yang sesuai dengan kebutuhkan salah satunya dengan menerapkan langkah-langkah sebagai berikut: memisahkan setiap kata pada kalimat, memberikan penanda untuk setiap kata, mengklasifikasn kata yang serupa melalui pemberian tag-tag tertentu.

Langkah 2: Mengestimasi parameter HMM
Terdapat empat buah tahapan untuk langkah kedua, yaitu:
1. Mencari states: Pada tahap ini, setiap kelompok kata yang telah diklasifikan di langkah pertama akan diproses berdasarkan tag-nya. Keluaran dari proses adalah berupa state vector;
2. Melakukan kalkukasi start probability, π: Start probability dapat dihitung dengan rumus x/y, dengan x adalah banyaknya kalimat yang dimulai dengan tag tertentu dan y adalah banyaknya kalimat pada text. Tahap ini dilakukan untuk setiap tag yang ada;
3. Melakukan kalkukasi transition probability, A: Transition probability dapat dihitung dengan rumus x/y, dengan x adalah banyaknya ofsequences dari Ti ke Tj dan y adalah jumlah Ti. Tahap ini dilakukan untuk setiap tag yang ada;
4. Melakukan kalkukasi emission probability, B: Emission probability dapat dihitung dengan rumus x/y, dengan x adalah banyaknya kemunculan kata pada teks dan y adalah total kemunculan tag tersebut pada teks. Tahap ini dilakukan untuk setiap tag yang ada.

Langkah 3: Melakukan testing
Setelah selesai melakukan kalkukasi terhadap parameter-parameter pada langkah kedua, gunakan algoritma viterbi berdasarkan masukan parameter yang dimiliki untuk mengobservasi masukan dengan outuput berupa kumpulan kata yang diidentifikasikan sebagai entitas.
