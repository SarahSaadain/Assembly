adding up lengths of all reads
```
nohup bash -c 'zless lengths.txt.gz | cut -f1 | paste -sd "+" |bc > total_bases.txt' & 
```
output: 122853180480

adding up lengths of all reads that were selected for the 100x
```
zless results/Dere_14062023_PAO93669_sorted_100x.fastq.gz | paste - - - - |  awk  '{print(length($2))}' | paste -sd "+" | bc > total_bases_100x.txt
```
output: 7248944852
