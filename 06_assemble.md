Assembly step
```
date
../canu-2.2/bin/canu corThreads=50 -p derecta -d results/canu_correct genomeSize=145m correctedErrorRate=0.14256 -trimmed -corrected -nanopore results/canu_correct/derecta.trimmedReads.fasta.gz
date
```

Check which files takes forever
```
for file in overlap.*.out; do grep -q "Bye" "$file" && echo "Found 'Bye' in $file" || echo "'Bye' not found in $file"; done
```
