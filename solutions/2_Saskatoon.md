https://sadservers.com/scenario/saskatoon

```bash
# using cut to take only IPs, uniq with counter and sorting, and tail for last one 
cut -d ' ' -f 1 /home/admin/access.log | sort | uniq -c | sort | tail -1
```

```bash
echo "66.249.73.135" > /home/admin/highestip.txt
```