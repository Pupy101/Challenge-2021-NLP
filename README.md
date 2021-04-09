# Кейс-чемпионат Changellenge >> Cup IT 2021
### Была поставлена задача обучения классификатора, который должен определять по входным данным (двум пердложениям) следующие классы:
1. entailment    (из параграфа 1 следует параграф 2)
2. contradiction (параграф 1 противоречит параграфу 2)
3. neutral       (в параграфе 1 и параграфе 2 содержится схожая по смыслу информация)

### Данные от Стэмфордского университета представлены в виде хорошо размеченного датасета в котором имеются обучающая/валиационная и тестовая выборки.
### Пример данных издатасета:
![image](https://user-images.githubusercontent.com/26460175/114156871-b25cc600-992b-11eb-87d4-23bd7a41dda9.png)

### Корпус был приведен к нижнему регистру и нормализован с помощью библиотеки spaCy, также была отброшена находившаяся в датасете разметка для графовых сетей.
После [предобработки](https://colab.research.google.com/drive/1jPQ6Kp78IJT1QpM4WqMLu-Y7igibc0E3?usp=sharing):
![image](https://user-images.githubusercontent.com/26460175/114157309-2eefa480-992c-11eb-9e6b-4a3634a8f2e4.png)

### Лэйблы данных распределены следующим образом:
![image](https://user-images.githubusercontent.com/26460175/114157387-42027480-992c-11eb-845a-fdf21412b343.png)

### Первой была обучена простая сверочная модель c 1D свертками:
![image](https://user-images.githubusercontent.com/26460175/114157715-9ad20d00-992c-11eb-9b1b-a93526b8bbfc.png)

#### Результаты CNN:
![image](https://user-images.githubusercontent.com/26460175/114157876-c94fe800-992c-11eb-8e45-65b89794db9b.png)

### Второй моделью стала рекуррентная сеть на основе BiLSTM:
![image](https://user-images.githubusercontent.com/26460175/114157803-b0dfcd80-992c-11eb-876b-ccb1dfe94cbd.png)

#### Результаты RNN:
![image](https://user-images.githubusercontent.com/26460175/114157918-d4a31380-992c-11eb-8a8d-b9f88c498b74.png)
#### [Ноутбук](https://colab.research.google.com/drive/1RbeB3GqFgBBwdlP1m3DL97tUADJqE8Ut?usp=sharing) с обучением.

### Третьей моделью была сделана рекуррентная сеть с изменённой архитектурой:
![image](https://user-images.githubusercontent.com/26460175/114158238-264b9e00-992d-11eb-8437-54d9fb44d3c2.png)

#### Результаты BiLSTM + feature generation:
![image](https://user-images.githubusercontent.com/26460175/114158511-6ad73980-992d-11eb-8b3c-d5d0652d7d0a.png)

[Ноутбук](https://colab.research.google.com/drive/1HQp7t6Axp_5iaxuFBJD3Z2VK_eb8b-cH?usp=sharing) обучения поледней модели.


