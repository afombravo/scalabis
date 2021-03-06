# Welcome to scalabis
A Python3 module for fast & easy sequence comparison

scalabis is built on numba and numpy, taking advantage of JIT compiled functions for speedy mismatched sequence comparisons.

# Instructions

Install scalabis using pip:

`pip install scalabis`

Import it as any other python module:

`import scalabis as sc`


Usage examples. See help(function) after import for more use details:

`sequence1 = "pihton"`

`sequence2 = "Hello there, this is a test for a fast & easy mismatch matching python module. Allegedly, it is efficient"`

count by how many mismatches 2 same lenght sequences diverge:

`sc.mismatch_counter(sequence1,sequence2)`

find one sequence in another, with mismatches. return_template=True returns 

`sc.find(sequence1,sequence2,mismatch=1)`

without return in a class

`sc.find(sequence1,sequence2,mismatch=2,dict_return=False)`

compare two sequences, searching from the search sequence from a specified starting point (default=0), 
returning the full aligned matrix whrere mismatches are 1, and matches are 0. 
Mismatches are the total mismatches in the compared matrix

`sc.comparefromfound(sequence1,sequence2,mismatch=0,start=0,dict_return=True)`

compare two sequences, returning all the locations in which they differ

`sc.compareandlocate(start=0,search=sequence1,template=sequence2)`

compare two sequences, returning the full aligned matrix. starting point can be specified

`sc.compare(search=sequence1,template=sequence2,start=0,dict_return=False)`
