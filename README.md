# Домашнее задание к занятию "`Вычислительные мощности. Балансировщики нагрузки`" - `Лугинина Виктория`

Стенд не поднят до конца

## Манифесты

- [main.tf](https://github.com/victorialugi/net/blob/main/main.tf)
- [variables.tf](https://github.com/victorialugi/net/blob/main/variables.tf)
- [versions.tf](https://github.com/victorialugi/net/blob/main/versions.tf)

## Что успело создаться

- VPC и public-подсеть `192.168.10.0/24`
- бакет Object Storage и публичный объект `cat.jpg`
- сервисный аккаунт для Instance Group
- группа `lamp-group` в статусе `ACTIVE`, размер `0 -> 3`

## Чего нет

- трёх ВМ: `yc compute instance list` пустой
- сетевого балансировщика
- проверки страницы и удаления ВМ

`terraform apply` ждал операцию создания группы около 30 минут и несколько раз завершился ошибкой:

```text
Error while waiting operation to create instance group: context deadline exceeded
