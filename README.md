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
&ensp;python generalGap.py -option -input
<br />
Option:<br />
  -i      input two sequence in command line argument<br />
  -g      gap value, default -1<br />
  -gp     gap penalty, default -1<br />
  -m      match score, default +1<br />
  -mm     mismatch score, default -1<br />
  -f      input file, status: disable [under construction]<br />
<br />
Example: <br />
  python generalGap.py -i ACACACTA AGCACACA -g -1<br />
<br />
Output:<br />
  General Gap Penalty, Needleman-Wunch Algorithm<br />
  SEQUENCE 1: ACACACTA<br />
  SEQUENCE 2: AGCACACA<br />
  gap           :  -1.0<br />
  gap penalty   :  -1.0<br />
  match score   :  1.0<br />
  mismacth score:  -1.0<br />
  -0.0    -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    -7.0    -8.0    <br />
  -1.0    1.0     0.0     -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    <br />
  -2.0    0.0     0.0     -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    <br />
  -3.0    -1.0    1.0     0.0     0.0     -1.0    -2.0    -3.0    -4.0    <br />
  -4.0    -2.0    0.0     2.0     1.0     1.0     0.0     -1.0    -2.0    <br />
  -5.0    -3.0    -1.0    1.0     3.0     2.0     2.0     1.0     0.0     <br />
  -6.0    -4.0    -2.0    0.0     2.0     4.0     3.0     2.0     2.0     <br />
  -7.0    -5.0    -3.0    -1.0    1.0     3.0     5.0     4.0     3.0     <br />
  -8.0    -6.0    -4.0    -2.0    0.0     2.0     4.0     4.0     5.0     <br />
  Sequence 1:  A _ C A C A C T A<br />
  Sequence 2:  A G C A C A C _ A<br />
  Score     :  5.0<br />
