PySSA
=====

Copyleft (c) 2013. Ridlo W. Wibowo
<ridlo.w.wibowo@gmail.com>

Program sequence alignment sederhana, 
berisi 3 algoritma dasar:
  - Smith-Waterman Algorithm
  - Needleman-Wunsch Algorithm
  - Gotoh Algorithm
untuk keperluan pembelajaran bioinformatika, 
sequence alignment pada DNA, RNA atau protein lain.

Usage:
  python generalGap.py [option] [input]
Option:
  -i      input two sequence in command line argument
  -g      gap value, default -1
  -gp     gap penalty, default -1
  -m      match score, default +1
  -mm     mismatch score, default -1
  -f      input file, status: disable [under construction]
                 
Example: 
  python generalGap.py -i ACACACTA AGCACACA -g -1

Output:
  General Gap Penalty, Needleman-Wunch Algorithm
  SEQUENCE 1: ACACACTA
  SEQUENCE 2: AGCACACA
  gap           :  -1.0
  gap penalty   :  -1.0
  match score   :  1.0
  mismacth score:  -1.0
  -0.0    -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    -7.0    -8.0    
  -1.0    1.0     0.0     -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    
  -2.0    0.0     0.0     -1.0    -2.0    -3.0    -4.0    -5.0    -6.0    
  -3.0    -1.0    1.0     0.0     0.0     -1.0    -2.0    -3.0    -4.0    
  -4.0    -2.0    0.0     2.0     1.0     1.0     0.0     -1.0    -2.0    
  -5.0    -3.0    -1.0    1.0     3.0     2.0     2.0     1.0     0.0     
  -6.0    -4.0    -2.0    0.0     2.0     4.0     3.0     2.0     2.0     
  -7.0    -5.0    -3.0    -1.0    1.0     3.0     5.0     4.0     3.0     
  -8.0    -6.0    -4.0    -2.0    0.0     2.0     4.0     4.0     5.0     
  Sequence 1:  A _ C A C A C T A
  Sequence 2:  A G C A C A C _ A
  Score     :  5.0
