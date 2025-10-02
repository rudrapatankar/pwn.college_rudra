# Data Manipulation

## Extracting Specific Sections of Text



### Solve
**Flag:** pwn.college{Y2sYwWwL5KiOWU10l6UOGIIguVx.01NxEzNxwiNxIzNzEzW}

first check for number of columns in /challenge/run. then cut the column that contains flag and print it using tr operator with -d and "/n"

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
4450 p
20665 w
18670 n
5001 .
8850 c
21506 o
1120 l
16692 l
18037 e
16481 g
13324 e
12911 {
8139 Y
27079 2
18331 s
16474 Y
25953 w
21841 W
30485 w
8617 L
355 5
6637 K
7734 i
32672 O
29009 W
11435 U
18885 1
24612 0
29194 l
28437 6
20616 U
10312 O
7645 G
11265 I
12210 I
25573 g
23981 u
11059 V
12150 x
8149 .
6365 0
23740 1
24479 N
28336 x
2223 E
12211 z
16996 N
18346 x
27260 w
12422 i
21281 N
12954 x
12979 I
12351 z
7059 N
23397 z
24252 E
17879 z
22610 W
32261 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{Y2sYwWwL5KiOWU10l6UOGIIguVx.01NxEzNxwiNxIzNzEzW}

```

### New Learnings
cut removes and display the text of specified column in given text

### References 
N.A.
