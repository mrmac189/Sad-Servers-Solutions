https://sadservers.com/scenario/saint-john
```bash
lsof -F | grep -rli /var/log/bad.log
ps -ef | grep badlog.py
kill -9 593
```

```bash
fuser -v  /var/log/bad.log
kill -9 593
```