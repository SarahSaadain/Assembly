sorting the fastq files based on the length.txt I created prior

```
#!/bin/bash

date

export TMPDIR=/home/vetlinux04/Sarah/temp

gzip -cd lengths.txt.gz | sort -nr --batch=100M | awk '{print $2"\n"$3"\n"$4"\n"$5}' | gzip -c > Dere_14062023_PAO93669_sorted.fastq.gz

date

```
submitted it with

```
nohup bash scripts/sorting.sh > sorting.log &
```
check if it worked

```
zless Dere_14062023_PAO93669_sorted.fastq.gz | head -12 | paste - - - - | awk '{print length($2)}'
```
