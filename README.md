# CyberOK_Skipa_ips

Раз [@cyberok-org](https://www.github.com/cyberok-org) отказываются отвечать на просьбы исключения из сканирований, отправляю в паблик список ip адресов для банов на FW

Одновременно с запуском Zmap с scan-**.skipa.cyberok.ru, VDS/VPS селектела и etc., в логах также начинают появляться интересные сурсы - 212.192.158.0/24, с которых так же запускается Zmap:

![NGFW](https://github.com/tread-lightly/CyberOK_Skipa_GTFO/blob/main/NGFW.png)

C идентичным количеством отправляемых пакетов - 12-13 (1/3 от 36 пакетов на хост, которые они отправляют: https://youtu.be/4wSxp7t6huA?si=O15rvlfQ2J6IWBaD&t=620):

![PACKETS](https://github.com/tread-lightly/CyberOK_Skipa_GTFO/blob/main/packets.png)

С интересным провайдером **FGUP GRCHC**:

![LOOKUP](https://github.com/tread-lightly/CyberOK_Skipa_GTFO/blob/main/lookup.png)

Что есть ничто иное как Федеральное государственное унитарное предприятие «Главный радиочастотный центр» - дочка РКН, ответственная за мониторинг и цензурирование рунета https://baj.media/ru/kiberpartizany-rasskazali-kak-v-rossii-sozdayut-botov-kotorye-razmeshchayut-prokremlevskie-3/. Только на phd2 про это не было ни слова, а жаль

Ответ увожаемого CEO сайберока:

![TG](https://github.com/tread-lightly/CyberOK_Skipa_GTFO/blob/main/tg.png)

При наличии у Вас аффилированных с ними и отсутствующих в списке IP адресов, предлагаю репортить их сюда для включения: 

[![telegram:](https://img.shields.io/badge/Telegram-@wladimirwakhrushew-blue)](https://t.me/wladimirwakhrushew)

Наиболее полный перечень активных IP адресов сканеров CYBEROK Skipa на май 2024:
```
185.224.230.0/24
212.192.158.0/24
188.68.217.207
212.41.12.45
212.41.12.46
212.41.12.47
212.41.12.48
212.41.13.23
212.41.13.24
212.41.13.25
31.131.251.106
31.131.251.235
31.131.255.205
31.131.255.206
31.131.255.207
31.131.255.208
31.131.255.209
31.131.255.210
31.131.255.211
31.131.255.212
31.131.255.240
37.9.13.54
37.9.13.84
37.9.13.105
37.9.13.217
45.146.167.56
45.146.167.68
45.146.167.105
45.146.167.237
45.92.176.94
45.92.176.129
45.92.176.143
45.92.176.144
45.92.176.145
45.92.177.113
45.92.177.127
45.92.177.237
45.93.20.45
45.93.20.79
45.93.20.104
45.93.20.109
45.93.20.126
45.93.20.148
45.93.20.229
45.93.20.103
62.84.116.11
62.84.116.13
62.84.116.34
62.84.116.219
62.84.116.237
77.223.102.84
77.223.102.101
77.223.102.191
77.223.103.45
77.223.103.53
94.26.228.205
95.143.190.169
95.143.190.179
95.143.191.147
95.143.191.223
95.143.191.245
45.141.86.171
194.26.25.137
```

UPD 10.06.2024:

Замечена схожая активность с адреса ```45.141.86.171```. Потенциально, в сканированиях могут быть задействованы и адреса с подсети
```
45.141.86.0/24
```

UPD 04.07.2024:

Замечена схожая активность с адреса ```194.26.25.137```


