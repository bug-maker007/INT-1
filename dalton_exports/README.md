# Экспорты Dalton

Каждый архив - zip-экспорт задания Dalton: правила (`dalton-custom.rules`), конфиг Suricata и
`manifest.json`. В папку `results/` внутри архива добавлены результаты прогона: `alerts.txt`,
`rule_performance.txt` (профилирование правил), `ids_engine.txt` (вывод Suricata), `debug.txt`.

**ДАМПЫ УДАЛЕНЫ** из-за большого размера, все они лежат в ../pcaps/

Дампы очищены от трафика, не относящегося к агенту (см. раздел «Захват трафика» в REPORT.pdf).
Aggressive прогонялся вместе с prod, как его подключают на сенсоре.

| Архив | Набор | Suricata | Дампы |
| --- | --- | --- | --- |
| `suricata-8.0.7_prod_http_930c438743eb7bdf.zip` | prod_http | 8.0.7 | HTTP |
| `suricata-8.0.7_prod_https_1814827a054b60a3.zip` | prod_https | 8.0.7 | 4 × HTTPS |
| `suricata-8.0.7_aggressive_http_5e206a5d6d25bc22.zip` | prod_http + aggressive_http + aggressive_http_s8 | 8.0.7 | HTTP |
| `suricata-8.0.7_aggressive_https_554a36365dd3b4a7.zip` | prod_https + aggressive_https | 8.0.7 | 4 × HTTPS |
| `suricata-8.0.7_lab_ioc_899de064adb7e48e.zip` | lab_ioc | 8.0.7 | все 5 |
| `suricata-7.0.14_prod_http_8b87c854890ffec4.zip` | prod_http | 7.0.14 | HTTP |
| `suricata-7.0.14_prod_https_5a0084a26ade364c.zip` | prod_https | 7.0.14 | 4 × HTTPS |
| `suricata-7.0.14_aggressive_http_4fcc4b1c264a3a1c.zip` | prod_http + aggressive_http | 7.0.14 | HTTP |
| `suricata-7.0.14_aggressive_https_7bd213a3edcdffda.zip` | prod_https + aggressive_https | 7.0.14 | 4 × HTTPS |
| `suricata-7.0.14_lab_ioc_eafeadee3a5dfaa6.zip` | lab_ioc | 7.0.14 | все 5 |
| `suricata-8.0.7_AGRESSIVE_FINAL_b42bac36a75fc812.zip` | AGRESSIVE_FINAL (все 29 правил) | 8.0.7 | все 5 |
| `suricata-7.0.14_AGRESSIVE_FINAL_417df1b94d0dabfe.zip` | AGRESSIVE_FINAL (28 правил, 9200024 не загружается) | 7.0.14 | все 5 |
