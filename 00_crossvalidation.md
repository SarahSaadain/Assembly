adding up lengths of all reads
```
nohup bash -c 'zless lengths.txt.gz | cut -f1 | paste -sd "+" |bc > total_bases.txt' & 
```
output: 122853180480

fixed mistake:
```
taskset -c 0-10 gzip -cd results/Dere_14062023_PAO93669_sorted.fastq.gz | paste - - - - |  awk 's<14500000000 {s+=length($2);print $1; print $2; print $3; print $4}' | gzip  > results/Dere_14062023_PAO93669_sorted_100x.fastq.gz
```

adding up lengths of all reads that were selected for the 100x
```
zless results/Dere_14062023_PAO93669_sorted_100x.fastq.gz | paste - - - - |  awk  '{print(length($2))}' | paste -sd "+" | bc > total_bases_100x.txt
```
old output: 7248944852

idealy it should be: 14 500 000 000

new output: 14 500 076 338
