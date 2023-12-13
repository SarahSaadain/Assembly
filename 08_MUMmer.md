follow instructions here:
http://assemblytics.com

I used the recommended assembly from NCBI (but not the right strain of D.ere)
its the reference assembly from NCBI & is made by three different files
first I need to be in nucmer_outputs (on my computer in documents)
```
./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../ref_strain_dere_GCF_003286155.1_DereRS2_genomic.fna ../derecta.contigs.fasta -prefix 1_dere_vs_ref_assembly &
```

then:
```
gzip 1_dere_vs_ref_assembly.delta
```

data found here:
http://assemblytics.com/analysis.php?code=nHxkFG9Mxuvdm1dkSiJF



here I used the right strain (careful its the only one with GCA input file not GCF)
```
./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../same_strain_GCA_018904525.1_ASM1890452v1_genomic.fna ../derecta.contigs.fasta -prefix 1_dere_vs_dere_assembly & 
```
then:
```
gzip  1_dere_vs_dere_assembly.delta
```

data found here:
http://assemblytics.com/analysis.php?code=rOjgrbQfD3Io4vZ0ACkn


here I used Dmel
```
nucmer_outputs % ./../softwares/MUMmer3.23/nucmer -maxmatch -l 100 -c 500 ../dmel_GCF_000001215.4_Release_6_plus_ISO1_MT_genomic.fna ../derecta.contigs.fasta -prefix 1_dere_dmel_assembly &
```
then:
```
gzip 1_dere_dmel_assembly.delta
```

data found here:
http://assemblytics.com/analysis.php?code=sxal50HQGfEz3eHYnUqf
