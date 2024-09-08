```bash
cd clmystery/
cat README.md 
cat instructions 
cd mystery/
grep CLUE crimescene 

# we have two clues: a man and Anabell 
cat people
# there are two Annabels: Sun and Church
grep Annabel people
cat vehicles | grep Annabel
# both have vehicles 
cat vehicles | grep -n Annabel
vim vehicles 

# meanwhile checking memberships on common people in all 4 lists
# perfect for comm command, but it can take only 2 files as arguments and also sorted
cd memberships/
grep CLUE ../crimescene 
comm -12 <(sort Museum_of_Bash_History) <(sort Rotary_Club) > 1
comm -12 <(sort 1) <(sort Delta_SkyMiles) > 2
comm -12 <(sort 2) <(sort Terminal_City_Library) > 3
```