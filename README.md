# Functions for acquiring and calculating custom metrics for high school players from MaxPreps
Includes a table of url's for every varisty team in the United States as well as code for acquiring individual and team-level batting and pitching statistics based on those urls.

###Example

Run the `R` script to load the functions and the lookup table into your `R` session.

For individual batting statistics for the Buchanan Bears varisty team, you can use the `maxpreps_batting_ind` function:

``` r
> maxprep_batting_ind("http://www.maxpreps.com/high-schools/buchanan-bears-(clovis,ca)/baseball/stats.htm") %>%
    select(Team:Athlete.Name, OBP:SBper)
             Team city_state number       Athlete.Name  PA   OBP   SLG   OPS SB SBA BABIP  Kper BBper SBper
1  buchanan bears clovis, ca      1     B. Hormel (Fr)  10 0.500 0.666 1.167  0   0 0.444 0.000 0.100   NaN
2  buchanan bears clovis, ca      2    A. Peralta (Sr)  91 0.440 0.453 0.893  2   2 0.424 0.143 0.099   1.0
3  buchanan bears clovis, ca      3   C. Rocamora (Jr)  61 0.517 0.500 1.017  1   2 0.500 0.164 0.164   0.5
4  buchanan bears clovis, ca      4    J. Friesen (Sr)  26 0.385 0.375 0.760  0   0 0.381 0.115 0.077   NaN
5  buchanan bears clovis, ca      5     J. Arruda (Sr) 110 0.445 0.461 0.907  8  10 0.382 0.109 0.155   0.8
6  buchanan bears clovis, ca      6    J. O'Guinn (Jr) 116 0.405 0.514 0.919  5   5 0.400 0.112 0.052   1.0
7  buchanan bears clovis, ca      8      P. Allen (Sr)  49 0.500 0.487 0.987  0   0 0.517 0.204 0.102   NaN
8  buchanan bears clovis, ca      9     K. Brisco (Sr)  12 0.417 0.444 0.861  0   0 0.250 0.083 0.167   NaN
9  buchanan bears clovis, ca     10      C. Lopez (Sr)  81 0.420 0.355 0.776  1   1 0.326 0.099 0.210   1.0
10 buchanan bears clovis, ca     11   C. Williams (Sr)  54 0.444 0.477 0.921  6   6 0.400 0.130 0.167   1.0
11 buchanan bears clovis, ca     12 F. Lanningham (Sr)   5 0.200 0.200 0.400  0   0 0.250 0.200 0.000   NaN
12 buchanan bears clovis, ca     14    J. Dittman (Sr)   1 0.000 0.000 0.000  0   0   NaN 1.000 0.000   NaN
13 buchanan bears clovis, ca     15      C. Olson (Jr)  12 0.333 0.200 0.533  0   0 0.200 0.000 0.167   NaN
14 buchanan bears clovis, ca     17    M. McGrady (Jr)  28 0.571 0.523 1.095  0   0 0.600 0.214 0.179   NaN
15 buchanan bears clovis, ca     18     T. Hormel (Jr)   2 0.000 0.000 0.000  0   0 0.000 0.000 0.000   NaN
16 buchanan bears clovis, ca     19      Q. Selma (Jr) 114 0.526 0.778 1.305  3   3 0.463 0.070 0.105   1.0
17 buchanan bears clovis, ca     20   K. McKenney (Jr)   1 1.000 0.000 1.000  0   0   NaN 0.000 1.000   NaN
18 buchanan bears clovis, ca     21      B. Wells (Jr)  13 0.385 0.545 0.930  0   0 0.333 0.308 0.000   NaN
19 buchanan bears clovis, ca     22   G. Gambrell (Sr) 111 0.423 0.610 1.033  0   0 0.400 0.126 0.090   NaN
20 buchanan bears clovis, ca     24      N. Rossi (Jr)   3 0.333 0.000 0.333  1   1   NaN 0.667 0.333   1.0
21 buchanan bears clovis, ca     25     Z. Presno (Jr) 107 0.514 0.623 1.137  2   2 0.358 0.168 0.224   1.0
```
