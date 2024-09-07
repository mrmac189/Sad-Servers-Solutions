```bash
grep -r "Alice" --include="*.txt" . | wc -l
```

```bash
grep -r "Alice" -include="*.txt" . | cut -d ":" -f 1 | sort | uniq -c | grep -n Alice
grep -n Alice ./1342-0.txt
vim ./1342-0.txt
/Alice
```