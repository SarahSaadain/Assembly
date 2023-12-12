install cmake for racon on vetlinux:
(when already in the racon/build)
```
./../../cmake-3.28.0-linux-x86_64/bin/cmake -DCMAKE_BUILD_TYPE=Release ..
```
first do minimap for racon:
```
#!/bin/bash
date
minimap2 -c -t 40 /home/vetlinux04/Sarah/results/canu_correct/derecta.contigs.fasta /home/vetlinux04/Sarah/results/Dere_14062023_PAO93669_sorted_100x.fastq.gz  > /home/vetlinux04/Sarah/results/derecta_minimap_racon.paf
date
```
then run racon:
```
#!/bin/bash
date
/home/vetlinux04/Sarah/softwares/racon/build/bin/racon -t 40 /home/vetlinux04/Sarah/results/Dere_14062023_PAO93669_sorted_100x.fastq.gz /home/vetlinux04/Sarah/results/derecta_minimap_racon.paf /home/vetlinux04/Sarah/results/canu_correct/derecta.contigs.fasta
date
```
