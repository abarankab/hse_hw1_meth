# hse_hw1_meth

[колаб](https://colab.research.google.com/drive/1qzvO8MXqGz-VJmJjl9BWOwZRfCPvppO1#scrollTo=I4JWS2QOxd_U)

## Сравнение fastqc

### Для начала посмотрим на обычные fastqc файлы взятые из какой-то старой домашки

![gc_normal](resources/gc_normal.png)
![per_base_normal](resources/per_base_normal.png)
![quality_normal](resources/quality_normal.png)

### Теперь посмотрим на fastqc BS-Seq

![gc_meth](resources/gc_meth.png)
![per_base_meth](resources/per_base_meth.png)
![quality_meth](resources/quality_meth.png)

Заметно отличается GC content — у BS-seq он далек от теоретического распредиления. Также у BS-seq более гладкое распределение по нуклеотидам. Помимо этого, у BS-seq сильно падает качество к концу чтения.

## Статистики

Я сразу использовал параллельную дедупликацию, она в колабе.

### 8cell

* ридов на 11347700-11367700: 1090
* ридов на 40185800-40195800: 464
* дупликаций: 18.31%

### Epiblast

* ридов на 11347700-11367700: 2328
* ридов на 40185800-40195800: 1062
* дупликаций: 2.92%

### ICM

* ридов на 11347700-11367700: 1456
* ридов на 40185800-40195800: 630
* дупликаций: 9.08%

## M-bias

### 8cell
#### 1 рид
![8cell_read_1](resources/73_1.png)
#### 2 рид
![8cell_read_2](resources/73_2.png)

### Epiblast
#### 1 рид
![epiblast_read_1](resources/22_1.png)
#### 2 рид
![epiblast_read_2](resources/22_2.png)


### ICM
#### 1 рид
![icm_read_1](resources/75_1.png)
#### 2 рид
![icm_read_2](resources/75_2.png)

CPG составляет ~40% и ~20%.

## Гистограммы

Код по гистограмме также в colab.

### 8cell
![hist_73](resources/hist_73.png)

### Epiblast
![hist_73](resources/hist_22.png)

### ICM
![hist_73](resources/hist_75.png)

Уровень CPG совпадает с тем, что показывает гистограмма.

## Покрытие

![image_cov](resources/image_cov.png)

## Метилирование

![image_meth](resources/image_meth.png)
