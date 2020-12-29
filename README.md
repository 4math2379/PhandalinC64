#Phandalin  Adventures

***
** 
RPG game with my friend translate inside this basic adventure game text.

Dedicace for for Bobby Montano.
**************
## Movement inside the game 
###Data strucutres 
.2 NORTH 
.3 SOUTH
.4 UP
ETC ETC 


```
10 NM=13:R=13:VL=8:DIM NO$(NM),EX$(NM),M%(R,6),DE$(R)
15 DIM VB$(VL),LO(NM)
20 FOR X=1 TO NM:READ NO$(X):READ EX$(X):NEXT
1001 DATA"NORTH","
1002 DATA"SOUTH","
1003 DATA"EAST","
1004 DATA"WEST","
1005 DATA"UP","
1006 DATA"DOWN","
1007 DATA"LANTERN","
1008 DATA"OIL","
1009 DATA"ROPE","
1010 DATA"SWORD","
1011 DATA"RUBY","
1012 DATA"WERE RATS","
1013 DATA"WHITE DRAGON","
```



### verb list 

   ```
2100 FOR X=1 TO VL:READ VB$(X):NEXT
2101 DATA "GO","GET","DROP","INVENTORY","EXAMINE","READ"
2102 DATA "USE","LIGHT"
```
### DATA MORE MORE MORE 

```
3000 FOR X=1 TO R:READ DE$(X):NEXT
                              to 3013
```
line 10 got R=13 can and more content data by upgrade this variable.


   
   
   need to Parser the move of line 2101
```
100 v=0:n=0:ne$="":n$="":n2$="":v$="":v2=0:
a$="":pr=0:pt=0:nm=0:bz=0:FOR X=1 TO 10:wd$(x)="":NEXT x
101 INPUT A$:pt=1:nm=0:D$=A$:FOR a=1 TO LEN(D$)
102 IF MID$(D$, a, 1)=" " THEN A$=MID$(D$,pt,a-pt):
pt=a+1:nm=nm+1:wd$(nm)=A$
103 NEXT a:nm=nm+1:a$=MID$(D$,pt,a-pt):wd$(nm)=A$
104 v$=wd$(1):n$=wd$(2):IF wd$(3)="and" OR
wd$(3)="then" THEN v2$=wd$(4):n2$=wd$(5):co=1
105 IF wd$(3)="in" OR wd$(3)="from" OR wd$(3)="to"
THEN v$=wd$(1):ne$=wd$(2):pr=1:bz=1
```
   


                      


   
