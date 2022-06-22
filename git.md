# Git scripts

Sort authors by commits on specific files:

```shell
find -EL <path> -type f -regex '<file-regex>' | xargs -n 1 git blame --porcelain | grep  "^author " | sort | uniq -c | sort -nr | head -10
```
