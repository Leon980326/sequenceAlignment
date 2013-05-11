PySSA
=====

Copyleft (c) 2013. Ridlo W. Wibowo
<br \>
ridlo.w.wibowo@gmail.com

<br />
<br />
Sequence alignment adalah cara mengurutkan  sequence  asam amino pada DNA (Deoxyribonucleic acid), RNA (Ribonucleic acid), atau protein untuk mengidentifikasikan dearah kesamaan yang mungkin menjadi konsekuensi dari hubungan fungsional, struktural, dan evolusi antar  sequence.  Perkembangan algoritma dalam kasus bioinformatika sangat pesat  dan  tidak jarang  melibatkan komputasi besar untuk keperluan tertentu, semisal pencarian pada database protein.

<br />
Program sequence alignment sederhana (PySSA) ini menggunakan bahasa python dan berisi 3 algoritma dasar:
  - Smith-Waterman Algorithm
  - Needleman-Wunsch Algorithm
  - Gotoh Algorithm
untuk keperluan pembelajaran bioinformatika, sequence alignment pada DNA, RNA atau protein lain.

<br />
Usage:<br />
&ensp;&ensp;&ensp;&ensp;python generalGap.py -option -input
<br />
Option:<br />
  &ensp;&ensp;&ensp;&ensp;-i      &ensp;&ensp;&ensp;&ensp;input two sequence in command line argument<br />
  &ensp;&ensp;&ensp;&ensp;-g      &ensp;&ensp;&ensp;&ensp;gap value, default -1<br />
  &ensp;&ensp;&ensp;&ensp;-gp     &ensp;&ensp;&ensp;gap penalty, default -1<br />
  &ensp;&ensp;&ensp;&ensp;-m      &ensp;&ensp;&ensp;&ensp;match score, default +1<br />
  &ensp;&ensp;&ensp;&ensp;-mm     &ensp;&ensp;mismatch score, default -1<br />
  &ensp;&ensp;&ensp;&ensp;-f      &ensp;&ensp;&ensp;&ensp;input file, status: disable [under construction]<br />
<br />
Example: <br />
&ensp;&ensp;&ensp;&ensp;python generalGap.py -i ACACACTA AGCACACA -g -1<br />
<br />
Output:<br />
  &ensp;&ensp;&ensp;&ensp;General Gap Penalty, Needleman-Wunch Algorithm<br />
  &ensp;&ensp;&ensp;&ensp;SEQUENCE 1: ACACACTA<br />
  &ensp;&ensp;&ensp;&ensp;SEQUENCE 2: AGCACACA<br />
  &ensp;&ensp;&ensp;&ensp;gap           :  -1.0<br />
  &ensp;&ensp;&ensp;&ensp;gap penalty   :  -1.0<br />
  &ensp;&ensp;&ensp;&ensp;match score   :  1.0<br />
  &ensp;&ensp;&ensp;&ensp;mismacth score:  -1.0<br />
  &ensp;&ensp;&ensp;&ensp;-0.0    -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    -7.0    -8.0    <br />
  &ensp;&ensp;&ensp;&ensp;-1.0    1.0     0.0     -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    <br />
  &ensp;&ensp;&ensp;&ensp;-2.0    0.0     0.0     -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    <br />
  &ensp;&ensp;&ensp;&ensp;-3.0    -1.0    1.0     0.0     0.0     -1.0    -2.0    -3.0    -4.0    <br />
  &ensp;&ensp;&ensp;&ensp;-4.0    -2.0    0.0     2.0     1.0     1.0     0.0     -1.0    -2.0    <br />
  &ensp;&ensp;&ensp;&ensp;-5.0    -3.0    -1.0    1.0     3.0     2.0     2.0     1.0     0.0     <br />
  &ensp;&ensp;&ensp;&ensp;-6.0    -4.0    -2.0    0.0     2.0     4.0     3.0     2.0     2.0     <br />
  &ensp;&ensp;&ensp;&ensp;-7.0    -5.0    -3.0    -1.0    1.0     3.0     5.0     4.0     3.0     <br />
  &ensp;&ensp;&ensp;&ensp;-8.0    -6.0    -4.0    -2.0    0.0     2.0     4.0     4.0     5.0     <br />
  &ensp;&ensp;&ensp;&ensp;Sequence 1:  A _ C A C A C T A<br />
  &ensp;&ensp;&ensp;&ensp;Sequence 2:  A G C A C A C _ A<br />
  &ensp;&ensp;&ensp;&ensp;Score     :  5.0<br />

Untuk keperluan tugas saja.. :P
