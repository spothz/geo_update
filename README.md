# Обновление правил маршрутизации ядра xray.(geoip.dat, geosite.dat)

1. Автоматичее обновления правил geogeosite.dat и geoio.dat по пути /usr/share/xray/
из https://github.com/runetfreedom/russia-v2ray-rules-dat:

       cd /sbin && wget https://raw.githubusercontent.com/Spothz/clear_cache_openwrt/refs/heads/main/rules_update.sh

2. Выдать права:

	   chmod +x /sbin/rules_update.sh

3. Зайти в запланированные задачи и ввести:

	   0 3 */2 * * /sbin/rules_update.sh
  - обновлять раз в 2 дня в 3 часа ночи.

4. Перезагрузить cron:

       service cron restart
