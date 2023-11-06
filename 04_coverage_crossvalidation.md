adding up lengths of all reads
```
nohup bash -c 'zless lengths.txt.gz | cut -f1 | paste -sd "+" |bc > total_bases.txt' & 
```
output: 122853180480



fixed mistake: multiply the genome length by the coverage, in this case its 145 000 000 x 100 = 14 500 000 000

04_100x_coverage.sh
```
taskset -c 0-10 gzip -cd results/Dere_14062023_PAO93669_sorted.fastq.gz | paste - - - - |  awk 's<14500000000 {s+=length($2);print $1; print $2; print $3; print $4}' | gzip  > results/Dere_14062023_PAO93669_sorted_100x.fastq.gz
```

for 150x coverage multiply the genome length by the coverage is 145 000 000 x 150 = 21 750 000 000
04_150x_coverage.sh
                                                                                     
``` 
taskset -c 0-10 gzip -cd results/Dere_14062023_PAO93669_sorted.fastq.gz | paste - - - - |  awk 's<21750000000 {s+=length($2);print $1; print $2; print $3; print $4}' | gzip  > results/Dere_14062023_PAO93669_sorted_150x.fastq.gz
```
adding up lengths of all reads that were selected for the 100x

04_crosscheck_100x.sh
```
zless results/Dere_14062023_PAO93669_sorted_100x.fastq.gz | paste - - - - |  awk  '{print(length($2))}' | paste -sd "+" | bc > total_bases_100x.txt
```
old output: 7248944852
idealy it should be: 14 500 000 000
new output: 14 500 076 338
14 500 076 338/genome size=100.0005

04_crosscheck_150x.sh
```
zless results/Dere_14062023_PAO93669_sorted_150x.fastq.gz | paste - - - - |  awk  '{print(length($2))}' | paste -sd "+" | bc > total_bases_150x.txt
```
idealy it should be: 14 500 000 000

output: 
