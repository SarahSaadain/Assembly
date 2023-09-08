adding up lengths of all reads
```
nohup bash -c 'zless lengths.txt.gz | cut -f1 | paste -sd "+" |bc > total_bases.txt' & 
```
