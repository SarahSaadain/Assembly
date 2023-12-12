follow instructions here:
http://assemblytics.com

here I used the recommended assembly from NCBI (but not the right strain of D.ere), I called it dere_diffStrain_raw_assembly.delta.gz:
its the reference assembly from NCBI which is made by three different files
```
nucmer_outputs % ./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../ncbi_dataset_21/ncbi_dataset/data/GCF_003286155.1/GCF_003286155.1_DereRS2_genomic.fna ../derecta.contigs.fasta -prefix dere_diffStrain_raw_assembly
```

then:
```
gzip dere_raw_assembly.delta
```

data found here:
http://assemblytics.com/analysis.php?code=hVfAiBU12iDW0RReR7JH




here I used the right strain
```
./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../ncbi_dataset_22/ncbi_dataset/data/GCF_000001215.4/GCF_000001215.4_Release_6_plus_ISO1_MT_genomic.fna ../derecta.contigs.fasta -prefix dere_sameStrain_raw_assembly
```
then:
```
gzip dere_sameStrain_raw_assembly.delta
```

data found here:
http://assemblytics.com/analysis.php?code=kunH3OKw7Iq3h2HIgQHA


here I used Dmel
```
./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../ncbi_dataset_22/ncbi_dataset/data/GCF_000001215.4/GCF_000001215.4_Release_6_plus_ISO1_MT_genomic.fna ../derecta.contigs.fasta -prefix dere_dmel_raw_assembly
```
then:
```
gzip dere_dmel_raw_assembly.delta
```

data found here:
http://assemblytics.com/analysis.php?code=vPVLDF0ACzQ9gVptUhuc
