install cmake for racon on vetlinux:
(when already in the racon/build)
```
./../../cmake-3.28.0-linux-x86_64/bin/cmake -DCMAKE_BUILD_TYPE=Release ..
```
copy stuff on vetlinux:
```
scp /Users/ssaadain/Downloads/ncbi_dataset_21/ncbi_dataset/data/GCA_003286155.2/GCA_003286155.2_DereRS2_genomic.fna vetlinux04@pgnsrv042.vu-wien.ac.at:/home/vetlinux04/Sarah
```
