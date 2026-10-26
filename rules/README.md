# Правила Suricata: Mythic C2 v3.4.36, HTTP C2 Profile, агент Medusa

Формат сообщений: `C2 Mythic <что происходит> (<конкретный признак>)`.

| Папка / файл | Правил | sid | Назначение |
| --- | --- | --- | --- |
| `prod/prod_http.rules` | 7 | 91000xx | повседневная работа, открытый HTTP или HTTP после TLS-инспекции |
| `prod/prod_https.rules` | 2 | 91000xx | повседневная работа, HTTPS без расшифровки |
| `aggressive/aggressive_http.rules` | 10 | 92000xx | дополнение к `prod_http.rules`: максимальное покрытие HTTP |
| `aggressive/aggressive_http_s8.rules` | 1 | 9200024 | дополнение к `aggressive_http.rules`, только Suricata 8+ (`entropy`) |
| `aggressive/aggressive_https.rules` | 3 | 92000xx | дополнение к `prod_https.rules`: максимальное покрытие HTTPS |
| `lab_ioc/lab_ioc.rules` | 6 | 93000xx | IOC тестового стенда (домены, UUID). **Не для боевых сенсоров** |
| `AGRESSIVE_FINAL.rules` | 29 | все | все правила выше одним файлом: самое полное детектирование при анализе дампа. Включает lab IOC, поэтому на боевые сенсоры не ставится |

