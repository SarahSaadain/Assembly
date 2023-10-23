Cleans the header from the fastq files to remove the unnecessary parts

```
#!/bin/bash
date

zless fastq/Dere_14062023_PAO93669.fastq.gz  | cut -f1 -d " " | gzip -c > fastq/Dere_14062023_PAO93669_clean.fastq.gz

date
```

and then to submit the script

```
nohup bash scripts/clean_header.sh > clean_header.log &
```


