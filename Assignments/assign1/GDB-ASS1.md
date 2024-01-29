1) gcc a.c b.c -I. -g -o out
2) break f1
3) break b.c:10
4) continue
5) 6 times
6) 3 times
7) info breakpoints <breakpointNumber>
8) info breakpoints
9) 33; ignore 1 2, r, c until breakpoint 1 hits, p x
10) set listsize 5, break f0, c, list