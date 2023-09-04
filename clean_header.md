Cleans the header from fastq files to remove the unnecessary parts (there were was tab separated parts from teh sequencing facility)

```
#!/bin/bash
date

zless fastq/Dere_14062023_PAO93669.fastq.gz  | cut -f1 -d " " | gzip -c > fastq/Dere_14062023_PA$

date
```
