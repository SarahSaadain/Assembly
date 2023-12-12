follow instructions here:
http://assemblytics.com

here I used the recommended assembly from NCBI (but not the right strain of D.ere), I called it dere_diffStrain_raw_assembly.delta.gz:
```
nucmer_outputs % ./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../ncbi_dataset_21/ncbi_dataset/data/GCF_003286155.1/GCF_003286155.1_DereRS2_genomic.fna ../derecta.contigs.fasta -prefix dere_raw_assembly
```

then:
```
gzip dere_raw_assembly.delta
```

here I used the right strain
```
./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../ncbi_dataset_22/ncbi_dataset/data/GCF_000001215.4/GCF_000001215.4_Release_6_plus_ISO1_MT_genomic.fna ../derecta.contigs.fasta -prefix dere_raw_assembly
```
then:
```
gzip dere_raw_assembly.delta
```
