adding up lengths of all reads
```
zless lengths.txt.gz | cut -f1 | paste -sd "+" |bc
```
