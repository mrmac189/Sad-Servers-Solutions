# Command Line Murders
https://sadservers.com/scenario/command-line-murders
- Kim and Harry back in business! With the help of CLI-tools.

```bash
# suspect was member of groups, we can find names which are listed in all 4 files with help of uniq
cd memberships/
cat Rotary_Club Delta_SkyMiles Terminal_City_Library Museum_of_Bash_History | sort | uniq -c | grep 4 > ../case
# we have witness
cat people | grep Annabel | grep F | head -2 >> case
cat streets/Hart_Place | head -40 | tail -1 >> case
cat interviews/interview-47246024
# valuable info about car
cat interviews/interview-699607 | tail -2 >> case
# using grep we can filter suitable cars
cat vehicles | grep -n L337 -A 5 | grep Honda -A 4 | grep Blue -A 3 | grep Owner | cut -d ":" -f 2 >> case

# we have now driver names and member names, we can compare those to find a person that has the car and a member of 4 groups
cat case | grep 4 | head -23 |cut -d ' ' -f 8-10 |sort > members 
cat case |tail -6 | sort |awk '{print $1,$2}' > drivers
# comm helps find same entries in both files
comm -12 members drivers
grep "Joe Germuska" people
cat streets/Plainfield_Street | head -275 | tail -1
cat interviews/interview-29741223
echo "Joe Germuska" > ~/mysolution
```