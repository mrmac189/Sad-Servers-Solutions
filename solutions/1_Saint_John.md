https://sadservers.com/scenario/saint-john

`lsof`and `fuser` are widely used to determine which process is using a file. 

## lsof approach
```bash
#more portable solution
lsof -F | grep -rli /var/log/bad.log
ps -ef | grep badlog.py
kill -9 593
```

## fuser approach
```bash
#more specified and elegant
fuser -v /var/log/bad.log
kill 593
```