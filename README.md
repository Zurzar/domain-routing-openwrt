Это ФОРК!!! Оригинальный скрипт в шапке темы и у разработчика !!!!
==============================================================

Что сделано !

[+] Добавлены свои списки для обхода блокировок.

[+] Реализовано новое дополнение - внесение всех поддоменов Cloudflare в списки на принудильное проксирование трафика. Инфо https://habr.com/ru/news/922532/ 

# Описание
Автоматизируют настройку роутера на OpenWrt для роутинга по доменам и спискам IP-адресов.

# Скрипт для установки
```
sh <(wget -O - https://github.com/Zurzar/domain-routing-openwrt/blob/master/getdomains-install.sh)
```

# Скрипт для удаления
```
sh <(wget -O - https://raw.githubusercontent.com/Zurzar/domain-routing-openwrt/refs/heads/master/getdomains-uninstall.sh)
```

## Скрипт для проверки конфигурации
Написан для OpenWrt 23.05 и 22.03. На 21.02 работает только половина проверок.

[x] - не обязательно означает, что эта часть не работает. Но это повод для ручной проверки.

### Запуск
```
wget -O - https://raw.githubusercontent.com/Zurzar/domain-routing-openwrt/master/getdomains-check.sh | sh
```

По-умолчанию запускается на русском языке. Если нужно запустить на английском, то после `sh` нужно добавить `-s --lang en`. Аналогично для проверок на подмену DNS и создания дампа.

```
wget -O - https://raw.githubusercontent.com/Zurzar/domain-routing-openwrt/master/getdomains-check.sh | sh -s --lang en
```

### Запустить с проверкой на подмену DNS
```
wget -O - https://raw.githubusercontent.com/Zurzar/domain-routing-openwrt/master/getdomains-check.sh | sh -s dns
```
