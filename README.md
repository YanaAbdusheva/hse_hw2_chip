# hse_hw2_chip
Для выполнения задания была выбрана клеточная линия - **MM.1S**, гистоновая метка - **H3K4me3** (ссылка https://www.encodeproject.org/experiments/ENCSR361FWQ/)

Реплика 1: ENCFF575KIT 
Реплика 2: ENCFF755VRL
Контроль:  ENCFF169TIB 

Ссылка на Colab: https://colab.research.google.com/drive/1y4ONIeQsVcQudiZxSL2GHYDNPa0wTarx?usp=sharing

# Анализ Fastq
## ENCFF575KIT.fastq
Исходя из графиков Per base sequence quality и Per tile sequence quality (отмечены как непрошедшие проверку качества), для данного чтения было необходимо провести подрезание (с использованием trimmomatic)

До:

![КИТ_ДО_БЭСИК](https://user-images.githubusercontent.com/93256219/156249047-92f6e6b1-5d23-45d1-966e-2dcb7b28ae6e.png)
![KIT_до](https://user-images.githubusercontent.com/93256219/156245397-3abd3916-0c0e-4688-b0ee-2129988b3801.png)
![КИТ_до_тиле](https://user-images.githubusercontent.com/93256219/156249131-c9c3823a-fdd6-4b43-9cb1-6faac7fb5419.png)


После (ситуация улучшилась): 

![КИТ_ПОСЛЕ_БЭСИК](https://user-images.githubusercontent.com/93256219/156249159-3578f703-53f4-42d7-aed7-2471cc632077.png)
![KIT_после](https://user-images.githubusercontent.com/93256219/156245443-ea64cbe6-df20-4561-9972-fa3adf761a58.png)
![КИТ_после_тиле](https://user-images.githubusercontent.com/93256219/156249259-7c475036-c937-470d-906b-07d121eb72af.png)

## ENCFF755VRL.fastq
Для данного чтения также было проведено подрезание с использованием trimmomatic

До:

![ВРЛ_ДО_БЭСИК](https://user-images.githubusercontent.com/93256219/156249785-a15d677b-f9fa-449c-ad33-23163d6a94ae.png)
![VRL_до](https://user-images.githubusercontent.com/93256219/156245569-aeea20c9-7048-4fb4-b950-56e59a27b2ad.png)
![ВРЛ_ДО_ТИЛЕ](https://user-images.githubusercontent.com/93256219/156249805-d9e32491-e6f0-4209-abef-6248e9f485f6.png)

После (ситуация улучшилась, но не намного):

![ВРЛ_ПОСЛЕ_БЭСИК](https://user-images.githubusercontent.com/93256219/156249849-21b616fa-b6b4-4591-869b-832f732b7de2.png)
![VRL_после](https://user-images.githubusercontent.com/93256219/156245582-4f5dc9ad-c48b-4b63-a311-d8b80e07c7ba.png)
![ВРЛ_ПОСЛЕ_ТИЛЕ](https://user-images.githubusercontent.com/93256219/156249869-3124de88-5b75-4f7e-8c8d-d50ab129958a.png)


## ENCFF169TIB.fastq
Для данного чтения подрезания не потребовалось 

![тиб_1](https://user-images.githubusercontent.com/93256219/156250016-40845a5d-3a9f-487c-91bf-eba4958081c3.png)
![TIB_OK](https://user-images.githubusercontent.com/93256219/156245677-ffea3fb8-1446-4c02-ab2b-73282822b50c.png)
![тиб_3](https://user-images.githubusercontent.com/93256219/156250024-1b634a5d-8c7c-493e-bb68-411146c96e50.png)


# Анализ выдачи bowtie

ChIP-seq | Общее количество ридов | Кол-во ридов, которые выравнились уникально | Кол-во ридов, которые выравнились не уникально | Кол-во ридов, которые не выравнились | 
 --- |--- |--- |--- |--- 
ENCFF575KIT_trimmed	 | 11546030	| 325720 (2.82%) | 980127 (8.49%)	| 10240183 (88.69%) |
ENCFF755VRL_trimmed | 9250754 | 245483 (2.65%) | 610508 (6.60%) | 8394763 (90.75%) |
ENCFF169TIB | 28221235	 | 914798 (3.24%) | 3600159 (12.76%) | 23706278 (84.00%) |

Почему процент выравниваний получился именно таким?

