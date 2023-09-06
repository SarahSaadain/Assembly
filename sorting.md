```
sorting the fastq files from longest to shortest read

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

