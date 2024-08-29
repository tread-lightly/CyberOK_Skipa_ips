# CyberOK Skipa ips & something more

Раз [@cyberok-org](https://www.github.com/cyberok-org) отказываются отвечать на просьбы исключения из сканирований, сливаю в паблик свой небольшой ресёрч и список аффилированных с ними ip адресов

## Про связь с подведами РКН

Начну с небольшой базы от увожаемого CEO сайберока (TL;DR: правильным является 4 вариант)

![TG](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/tg.png)

**Теперь факты:**

В первом и втором кварталах 2024, одновременно с запуском Zmap с scan-**.skipa.cyberok.ru, VDS/VPS селектела и etc., в логах регулярно светились интересные сурсы - 212.192.158.0/24, с которых так же запускался Zmap:

>... protection_name:"ZMap Security Scanner"; protection_type:"IPS"; proxy_src_ip:"212.192.158.168"; ser_agent_kid:"Other: Mozilla/5.0 zgrab/0.x"; service:"443"; ...
>
>
>... protection_name:"ZMap Security Scanner"; protection_type:"IPS"; proxy_src_ip:"77.223.120.227"; ser_agent_kid:"Other: Mozilla/5.0 zgrab/0.x"; service:"80"; ...

![NGFW](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/NGFW.png)


Количество отправляемых пакетов как хостами скипы, так и хостами из подсети 212.192.158.0/24, идентичное: 12-13 (1/3 от 36 пакетов на хост, которые они высылают: https://youtu.be/4wSxp7t6huA?si=O15rvlfQ2J6IWBaD&t=620 и нет, это не ограничения самого Zmap):

![PACKETS](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/packets.png)

Провайдером же подсети 212.192.158.0/24 является **FGUP GRCHC**, что есть ничто иное как Федеральное государственное унитарное предприятие «Главный радиочастотный центр» - дочка РКН, которую не раз связывали с мониторингом и цензурированием рунета https://baj.media/ru/kiberpartizany-rasskazali-kak-v-rossii-sozdayut-botov-kotorye-razmeshchayut-prokremlevskie-3/. Только на phd2 про таких "знакомых" не было ни слова, а жаль:

![LOOKUP](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/lookup.png)

Посмотреть на архивные репорты и периоды активности хостов ГРЧЦ можно на abuseipdb: https://www.abuseipdb.com/check-block/212.192.158.0/24

## Вычисляем по IP

Наиболее полный перечень активных IP адресов сканеров CYBEROK Skipa (обновляется регулярно):
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
77.223.120.227
194.26.25.137
82.148.21.205
94.26.228.18
5.188.159.228
80.249.131.92
176.208.67.114
```

UPD 10.06.2024:

Замечена схожая активность с адреса ```45.141.86.171```. Потенциально, в сканированиях могут быть задействованы и адреса с подсети
```
45.141.86.0/24
```

UPD 04.07.2024:

Добавлен ```77.223.120.227``` (scan-03.skipa.cyberok.ru)

Замечена схожая активность с адреса ```194.26.25.137```

UPD 18.07.2024:

Добавлен ```82.148.21.205``` (scan-04.skipa.cyberok.ru)

UPD 07.08.2024:

Добавлен ```94.26.228.18``` (scan-06.skipa.cyberok.ru)

UPD 18.08.2024:

Добавлен ```5.188.159.228```
(scan-05.skipa.cyberok.ru)

Добавлен ```80.249.131.92```
(scan-07.skipa.cyberok.ru)

UPD 29.08.2024:

Добавлен ```176.208.67.114```
(Zmap + идентичный характер отправки пакетов + пересечение по времени с хостами Skipa и FGUP GRCHC. Впервые замечен 14.04.2024)
