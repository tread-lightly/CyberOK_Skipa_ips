# CyberOK Skipa ips & something more

Раз [@cyberok-org](https://www.github.com/cyberok-org) отказываются отвечать на просьбы исключения из сканирований, сливаю в паблик свой небольшой ресёрч и список аффилированных с ними ip адресов

## Про связь с подведами РКН

Начну с [небольшой базы](https://t.me/poxek/4149?comment=85901) от увожаемого CEO сайберока (TL;DR: правильным является 4 вариант)

![TG](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/media/tg.png)

**Теперь факты:**

В первом и втором кварталах 2024, одновременно с запуском Zmap с scan-**.skipa.cyberok.ru, VDS/VPS селектела и etc., в логах начали регулярно светиться интересные сурсы - 212.192.158.0/24, с которых так же запускался Zmap:

>... protection_name:"ZMap Security Scanner"; protection_type:"IPS"; proxy_src_ip:"212.192.158.168"; ser_agent_kid:"Other: Mozilla/5.0 zgrab/0.x"; service:"443"; ...
>
>
>... protection_name:"ZMap Security Scanner"; protection_type:"IPS"; proxy_src_ip:"77.223.120.227"; ser_agent_kid:"Other: Mozilla/5.0 zgrab/0.x"; service:"80"; ...

![NGFW](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/media/NGFW.png)

Количество отправляемых пакетов как хостами скипы, так и хостами из подсети 212.192.158.0/24, идентичное: 12-13 - 1/3 от 36 пакетов на хост, которые они высылают ([выступление на phd2](https://youtu.be/4wSxp7t6huA?si=O15rvlfQ2J6IWBaD&t=620)) и нет, это не ограничения самого Zmap:

![PACKETS](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/media/packets.png)

Провайдером же подсети 212.192.158.0/24 является **FGUP GRCHC**, что есть ничто иное как Федеральное государственное унитарное предприятие «Главный радиочастотный центр» - дочка РКН, которую не раз связывали с мониторингом и цензурированием рунета ([источник](https://baj.media/ru/kiberpartizany-rasskazali-kak-v-rossii-sozdayut-botov-kotorye-razmeshchayut-prokremlevskie-3/)). Только на phd про таких "знакомых" не было ни слова, а жаль:

![LOOKUP](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/media/lookup.png)

Посмотреть на архивные репорты и периоды активности хостов ГРЧЦ можно на [abuseipdb](https://www.abuseipdb.com/check-block/212.192.158.0/24)

С политикой active probing сайберока монжо ознакомиться [здесь](https://www.cyberok.ru/policy.html). Очевидно, что запрос на исключение, как и блокировка только хостов scan-xx.skipa.cyberok.ru - это полумеры
> The moral of the story is: I chose a half-measure when I should have gone all the way. I'll never make that mistake again. No more half-measures, Walter. *(Season 3, Episode 12 of Breaking Bad)*

## IP адреса

Наиболее полный перечень активных IP адресов сканеров CYBEROK Skipa, ГРЧЦ и НКЦКИ (обновляется регулярно, помимо него доступны ip-листы в 3 разных форматах: [CIDR](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/lists/skipa_cidr.txt), [Range](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/lists/skipa_range.txt) и [CheckPointCSV](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/lists/skipa_checkpoint.csv)):
```
5.143.224.100/30
5.143.224.104/30
185.224.228.0/24
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
94.25.46.114
95.167.197.242
95.167.199.34
95.167.199.90
95.167.200.10
176.208.65.146
176.208.67.114
176.211.48.242
178.185.170.42
178.185.216.114
178.185.234.162
178.185.235.58
178.185.238.154
178.185.238.178
178.185.241.114
176.211.56.130
176.211.103.178
92.124.109.218
85.175.69.50
95.167.62.66
176.100.243.247
176.208.69.226
176.208.70.162
176.208.79.82
176.210.118.218
176.211.46.130
176.211.47.122
176.211.51.218
178.185.133.251
178.185.202.130
178.185.202.162
178.185.228.58
178.185.235.74
178.185.239.50
178.185.239.58
178.185.241.98
212.164.59.250
213.59.217.242
217.65.82.18
85.175.147.234
91.122.177.241
95.167.133.10
95.167.148.18
95.167.186.2 
95.167.198.186
95.167.62.82
95.167.82.26
95.167.87.66
95.189.36.106
80.93.187.17
5.178.87.167
```

UPD 10.06.2024:

Замечена схожая активность с адреса ```45.141.86.171```. Потенциально, в сканированиях могут быть задействованы и адреса с подсети ```45.141.86.0/24```

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

Добавлены ```176.208.67.114```, ```178.185.238.178```, ```178.185.238.154```, ```176.211.48.242```, ```176.208.65.146```, ```95.167.199.34```, ```178.185.170.42```, ```176.211.56.130```, ```178.185.235.58```, ```95.167.200.10```, ```178.185.241.114```, ```176.211.103.178```, ```94.25.46.114```, ```178.185.234.162```, ```178.185.216.114```, ```95.167.197.242```, ```95.167.199.90```
(Zmap + идентичный характер отправки пакетов + пересечение по времени с хостами Skipa и FGUP GRCHC. Впервые замечены в апреле 2024, а 28.08.2024 с большинства из них снова регистрируется трафик)


![PACKETS](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/media/28082024.png)


UPD 30.08.2024:

Добавлен ```92.124.109.218```

UPD 31.08.2024:

Добавлен ```85.175.69.50```

UPD 01.09.2024:

Добавлен ```95.167.62.66```

UPD 02.09.2024:

Добавлены ```176.100.243.247```, ```176.208.69.226```, ```176.208.70.162```, ```176.208.79.82```, ```176.210.118.218```, ```176.211.46.130```, ```176.211.47.122```, ```176.211.51.218```, ```178.185.133.251```, ```178.185.202.130```, ```178.185.202.162```, ```178.185.228.58```, ```178.185.235.74```, ```178.185.239.50```, ```178.185.239.58```, ```178.185.241.98```, ```212.164.59.250```, ```213.59.217.242```, ```217.65.82.18```, ```85.175.147.234```, ```91.122.177.241```, ```95.167.133.10```, ```95.167.148.18```, ```95.167.186.2 ```, ```95.167.198.186```, ```95.167.62.82```, ```95.167.82.26```, ```95.167.87.66```, ```95.189.36.106```
(Анализ репортов с AbuseIPDB + идентичный характер отправки пакетов + типичные провайдеры: sibirtelecom, rostelecom, avangarddsl)

![3RDPARTY](https://github.com/tread-lightly/CyberOK_Skipa_ips/blob/main/media/3rd_party_ips.png)

UPD 08.09.2024:

Добавлен диапазон ```5.143.224.100-5.143.224.107```. Прямой корреляции со скипой за несколько месяцев найти не удалось (кроме того, что используется Zmap). Немного вводных данных ([источник](https://gist.github.com/v98765/922793b6e5bfe0d9f7dd896337ab6952)):

> Сообщаем Вам, что во исполнение указа Президента РФ № 250 от 1 мая 2022 года и приказа ФСБ России № 213 от 11.05.2023, НКЦКИ на постоянной основе осуществляет сбор технических характеристик и параметров ресурсов сети Интернет принадлежащих участникам ГосСОПКА на предмет выявления угроз информационной безопасности Российской Федерации. Сбор технических характеристик и параметров осуществляется с использованием адресного пространства ПАО «Ростелеком» со следующих IP адресов:
>
> 5.143.224.100, 5.143.224.101, 5.143.224.102, 5.143.224.103, 5.143.224.104, 5.143.224.105, 5.143.224.106, 5.143.224.107
> 
> Данные  IP-адреса используются только для решения задач НКЦКИ.
> В связи с тем, что сбор технических характеристик и параметров может фиксироваться средствами обнаружения вторжений как компьютерные воздействия, просим не учитывать воздействия с вышеуказанных IP адресов.

Однако, сканируются не только участники госсопки ([репорты на abuseipdb](https://www.abuseipdb.com/check-block/5.143.224.0/24)). Лукацкий, к слову, тоже [связывал](https://lukatsky.ru/legislation/ot-bumazhnoy-ib-k-prakticheskoy-novyy-prikaz-fsb-po-monitoringu-zaschischennosti.html) этот приказ фсб с балалайкой сайберока ещё в 2023

UPD 09.09.2024:

Добавлены ```80.93.187.17``` (scan-06.skipa.cyberok.ru) и ```5.178.87.167``` (scan-08.skipa.cyberok.ru)
