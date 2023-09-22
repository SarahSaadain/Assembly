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
