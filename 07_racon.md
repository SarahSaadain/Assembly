install cmake for racon on vetlinux:
(when already in the racon/build)
```
./../../cmake-3.28.0-linux-x86_64/bin/cmake -DCMAKE_BUILD_TYPE=Release ..
```
copy stuff on vetlinux:
```
scp /Users/ssaadain/Downloads/ncbi_dataset_21/ncbi_dataset/data/GCA_003286155.2/GCA_003286155.2_DereRS2_genomic.fna vetlinux04@pgnsrv042.vu-wien.ac.at:/home/vetlinux04/Sarah
```

first do minimap for racon:
```
#!/bin/bash
date
minimap2 -c -t 40 /home/vetlinux04/Sarah/results/canu_correct/derecta.contigs.fasta /home/vetlinux04/Sarah/results/Dere_14062023_PAO93669_sorted_100x.fastq.gz  > /home/vetlinux04/Sarah/results/derecta_minimap_racon.paf
date
```
