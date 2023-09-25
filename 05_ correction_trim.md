first correct for nanopore
```
#!/bin/bash

date

./softwares/canu-2.2/bin/canu -correct corThreads=40 -p derecta -d results/canu_correct genomeSize=145m -nanopore results/Dere_14062023_PAO93669_sorted_100x.fastq.gz

date
```

then trim
```
(base) [vetlinux04@pgnsrv042 scripts]$ vi 05_trim.sh 

#!/bin/bash

date

./softwares/canu-2.2/bin/canu -trim corThreads=40  -p derecta -d results/canu_correct genomeSize=145m -corrected -nanopore results/canu_correct/derecta.correctedReads.fasta.gz

date
```
