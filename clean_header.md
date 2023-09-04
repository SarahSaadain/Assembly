Cleans the header from the fastq files to remove the unnecessary parts

(there were \t seperated information from the sequecning facility)

```
#!/bin/bash
date

zless fastq/Dere_14062023_PAO93669.fastq.gz  | cut -f1 -d " " | gzip -c > fastq/Dere_14062023_PA$

date
```
