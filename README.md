# Обновление правил маршрутизации ядра xray.(geoip.dat, geosite.dat)
## Для wget:
1. Скачать geogeosite.dat и geoio.dat https://github.com/runetfreedom/russia-v2ray-rules-dat в /usr/share/xray/:

       cd /sbin && wget https://raw.githubusercontent.com/spothz/geo_update_openwrt/refs/heads/main/rules_update.sh

2. Выдать права:

	   chmod +x /sbin/rules_update.sh

3. Зайти в запланированные задачи и ввести:

	   0 3 */2 * * /sbin/rules_update.sh
  - обновлять раз в 2 дня в 3 часа ночи.

4. Перезагрузить cron:

       service cron restart

## Для curl:

1. Скачать geogeosite.dat и geoio.dat https://github.com/runetfreedom/russia-v2ray-rules-dat в /usr/share/xray/:

       cd /sbin && wget https://raw.githubusercontent.com/spothz/geo_update_openwrt/refs/heads/main/rules_update_curl.sh

2. Выдать права:

	   chmod +x /sbin/rules_update_curl.sh

3. Зайти в запланированные задачи и ввести:

	   0 3 */2 * * /sbin/rules_update_curl.sh
  - обновлять раз в 2 дня в 3 часа ночи.

4. Перезагрузить cron:

       service cron restart
