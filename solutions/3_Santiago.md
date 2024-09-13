# Santiago
https://sadservers.com/scenario/santiago
- find/grep challenge with some cut and sort. 

##  1st iteration
```bash
# it's possible to omit find, grep can be recursive with -r
grep -r "Alice" --include="*.txt" . | wc -l
```

```bash
grep -r "Alice" -include="*.txt" . | cut -d ":" -f 1 | sort | uniq -c

# grep -n shows line number
grep -n Alice ./1342-0.txt

# manual but effective
vim ./1342-0.txt
/Alice
```

##  2nd iteration
Less manual intervention.
```bash
find /home/admin -name "*.txt" -exec grep Alice {} \; | wc -l 

```bash
FILE=$(find /home/admin -name "*.txt" -exec grep Alice {} \+ | cut -d ":" -f 1 | sort | uniq -c | sort | head -1 | awk '{print $2}')

grep -n Alice $FILE | awk '{print $1}' | cut -d ":" -f 1 | xargs -I {} tail -n +{} $FILE | head -2 | tail -1 | awk '{print $1}'

echo 411156 > /home/admin/solution
```

