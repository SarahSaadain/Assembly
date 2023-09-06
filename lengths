Getting the lengths of the reads

```
#!/bin/bash

date

taskset -c 0-3 gzip -cd fastq/Dere_14062023_PAO93669_clean.fastq.gz | taskset -c 4-6 paste - - - - | taskset -c 7-10 awk '{print length($2) "\t" $0}' | gzip -c >lengths.txt.gz

date
```


and then

```
nohup bash scripts/lengths_cores_assigned.sh > lengths.log &
```
