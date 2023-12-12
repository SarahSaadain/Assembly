first
```
gzip -cd toy.fastq.gz |paste - - - - | awk ‘{print length($2) “\t” $0}‘| sort -nr |gzip -c > toy.fastql.gz
```
then
```
cat toy.fastql|awk ‘s<20 {s+=$1;print $2; print $3; print $4; print $5}’
```

kill jobs
```
kill -9 <jobID>


copy stuff on vetlinux:
```
scp /Users/ssaadain/Downloads/ncbi_dataset_21/ncbi_dataset/data/GCA_003286155.2/GCA_003286155.2_DereRS2_genomic.fna vetlinux04@pgnsrv042.vu-wien.ac.at:/home/vetlinux04/Sarah
```
