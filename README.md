# SauresHA fix
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/chOng-m0rrino/sauresha-fix)](https://github.com/chOng-m0rrino/releases)
![GitHub Release Date](https://img.shields.io/github/release-date/chOng-m0rrino/sauresha-fix)
[![GitHub](https://img.shields.io/github/license/chOng-m0rrino/sauresha-fix)](LICENSE)

[![Maintenance](https://img.shields.io/badge/Maintained%3F-Yes-brightgreen.svg)](https://github.com/chOng-m0rrino/sauresha-fix/graphs/commit-activity)
[![GitHub issues](https://img.shields.io/github/issues/chOng-m0rrino/sauresha-fix)](https://github.com/chOng-m0rrino/sauresha-fix/issues)


## Update:
   <br />1. Fix [Errno 104] Connection reset by peer
   <br />2. Fix binary sensors state values
   <br />3. Add Controller name detection - add support for R2 4.5, add default value for unknown revisions

   <br />Рекомендую в настройках указать:
```yaml
  scan_interval:
    minutes: 30
```
   Иначе могут быть блокировки в будущем.


## Содержание

* [Установка](#устнановка)
  * [Ручная установка](#ручная-установка)
  * [Установка через HACS](#hacs_установка)

Интеграция котроллеров [Saures](https://www.saures.ru) c [Home Assistant](https://www.home-assistant.io/)
# Описание

В настоящее время поддерживаются следующие типы устройств от Saurus
1. Счетчик холодной воды (м³) = sensor в Home Assistant
2. Счетчик горячей воды (м³) = sensor в Home Assistant
3. Счетчик газа (м³) = sensor в Home Assistant
4. Датчик протечки (0 – нет протечки, 1 - протечка) = binary_sensor в Home Assistant
5. Датчик температуры (градусы) = sensor в Home Assistant
6. Электро-шаровой кран управление (0 – открыться, 1 - закрыться) - поддерживается, switch в Home Assistant
7. Счетчик тепла (кВт*ч) = sensor в Home Assistant
8. Счетчик электричества (кВт*ч) (в том числе многотарифные) = sensor в Home Assistant
9. Сухой контакт (0 – деактивирован, 1 – активирован) = binary_sensor в Home Assistant
10. Электро-шаровой кран состояние (0 – не подключен модуль, 1 – неизвестное состояние, 2 – открыт, 3 - закрыт) = sensor в Home Assistant
11. Непосредственно сами контроллеры = sensor в Home Assistant

## Установка

### Ручная установка

1. Добавляем компонент в Home Assistant
   Распаковываем архив. Папку sauresha берем целиком и копируем в custom_components.
2. Осуществляем конфигурацию компонента в Home Assistant через GUI.
3. Перезагружаем HA

### HACS установка

1. Убедитесь, что [HACS](https://custom-components.github.io/hacs/) уже устновлен.
2. Перейдите на закладку SETTINGS
3. Введите https://github.com/chOng-m0rrino/sauresha-fix   и выберите категорию Integration, нажмите Сохранить
4. Новый репозиторий Integration Saures controllers with HA будет добавлен на закладке Integration
5. Устновите SauresHA из него
3. Осуществляем конфигурацию компонента в Home Assistant через GUI.
4. Перезапустите HA.
