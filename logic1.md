## Logic1

Basic boolean logic puzzles -- if else and or not

### cigar_party 

When squirrels get together for a party, they like to have cigars. A squirrel party is successful when the number of cigars is between 40 and 60, inclusive. Unless it is the weekend, in which case there is no upper bound on the number of cigars. Return True if the party with the given values is successful, or False otherwise.

cigar_party(30, False) → False</br>
cigar_party(50, False) → True</br>
cigar_party(70, True) → True

```
def cigar_party(cigars, is_weekend):
  if is_weekend and cigars>=40:
    return True
  elif (not is_weekend) and (cigars>=40 and cigars<=60):
    return True
  return False
```

### date_fashion 

You and your date are trying to get a table at a restaurant. The parameter "you" is the stylishness of your clothes, in the range 0..10, and "date" is the stylishness of your date's clothes. The result getting the table is encoded as an int value with 0=no, 1=maybe, 2=yes. If either of you is very stylish, 8 or more, then the result is 2 (yes). With the exception that if either of you has style of 2 or less, then the result is 0 (no). Otherwise the result is 1 (maybe).

date_fashion(5, 10) → 2</br>
date_fashion(5, 2) → 0</br>
date_fashion(5, 5) → 1

```
def date_fashion(you, date):
  if you <=2 or date<=2:
    return 0
  elif you>=8 or date>=8:
    return 2
  return 1
```

### squirrel_play

The squirrels in Palo Alto spend most of the day playing. In particular, they play if the temperature is between 60 and 90 (inclusive). Unless it is summer, then the upper limit is 100 instead of 90. Given an int temperature and a boolean is_summer, return True if the squirrels play and False otherwise.

squirrel_play(70, False) → True</br>
squirrel_play(95, False) → False</br>
squirrel_play(95, True) → True

```
def squirrel_play(temp, is_summer):
  if is_summer:
    return 60<=temp<=100
  else:
    return 60<=temp<=90
```