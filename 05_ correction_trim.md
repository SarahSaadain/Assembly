first correct for nanopore
```
#!/bin/bash

date

./softwares/canu-2.2/bin/canu -correct -p derecta -d results/canu_correct genomeSize=145m -nanopore results/Dere_14062023_PAO93669_sorted_100x.fastq.gz
```

then trim
```
```
