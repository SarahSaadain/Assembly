first correct for nanopore
```
#!/bin/bash

date

./softwares/canu-2.2/bin/canu -correct corThreads=40 -p derecta -d results/canu_correct genomeSize=145m -nanopore results/Dere_14062023_PAO93669_sorted_100x.fastq.gz

date
```

then trim (this script got stuck for 8 weeks)
```
(base) [vetlinux04@pgnsrv042 scripts]$ vi 05_trim.sh 

#!/bin/bash

date

./softwares/canu-2.2/bin/canu -trim corThreads=40  -p derecta -d results/canu_correct genomeSize=145m -corrected -nanopore results/canu_correct/derecta.correctedReads.fasta.gz

date
```

This is the script that actually worked (after 10 days) on Roco
```
date
../canu-2.2/bin/canu -trim corThreads=50 ovlMerDistinct=0.975 -p derecta -d results/canu_correct genomeSize=145m -trimmed -corrected -nanopore results/canu_correct/derecta.correctedReads.fasta.gz
date
```

This is the script that ran on vetlinux (finished in a few days) which additionally including a correctedErrorRate=0.085
```
date
../canu-2.2/bin/canu -trim corThreads=40 ovlMerDistinct=0.975 correctedErrorRate=0.085 -p derecta -d results/canu_correct genomeSize=145m -corrected -nanopore results/canu_correct/derecta.correctedReads.fasta.gz
date
```
Note:  
  on vetlinux I used the fast settings (ovlMerDistinct=0.975 and correctedErrorRate=0.085)  
  on Roco I used (ovlMerDistinct=0.975 but no specifics on maxerate)
