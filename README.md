# hse_hw2_chip
Для выполнения задания была выбрана клеточная линия - **MM.1S**, гистоновая метка - **H3K4me3**

Ссылка на Colab: https://colab.research.google.com/drive/1y4ONIeQsVcQudiZxSL2GHYDNPa0wTarx?usp=sharing

# Анализ Fastq
## ENCFF575KIT.fastq
Для данного чтения было проведено подрезание с использованием trimmomatic

До:

![KIT_до](https://user-images.githubusercontent.com/93256219/156245397-3abd3916-0c0e-4688-b0ee-2129988b3801.png)

После: 

![KIT_после](https://user-images.githubusercontent.com/93256219/156245443-ea64cbe6-df20-4561-9972-fa3adf761a58.png)

## ENCFF755VRL.fastq
Для данного чтения также было проведено подрезание с использованием trimmomatic

До:

![VRL_до](https://user-images.githubusercontent.com/93256219/156245569-aeea20c9-7048-4fb4-b950-56e59a27b2ad.png)

После:

![VRL_после](https://user-images.githubusercontent.com/93256219/156245582-4f5dc9ad-c48b-4b63-a311-d8b80e07c7ba.png)

## ENCFF169TIB.fastq
Для данного чтения подрезания не потребовалось 
![TIB_OK](https://user-images.githubusercontent.com/93256219/156245677-ffea3fb8-1446-4c02-ab2b-73282822b50c.png)

# Анализ выдачи bowtie

ChIP-seq | Общее количество ридов | Кол-во ридов, которые выравнились уникально | Кол-во ридов, которые выравнились не уникально | Кол-во ридов, которые не выравнились | 
 --- |--- |--- |--- |--- 
ENCFF575KIT_trimmed	 | 11546030	| 325720 (2.82%) | 980127 (8.49%)	| 10240183 (88.69%) |
ENCFF755VRL_trimmed | 9250754 | 245483 (2.65%) | 610508 (6.60%) | 8394763 (90.75%) |

