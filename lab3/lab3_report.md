University: ITMO University

Faculty: FICT

Course: IP-Telephony

Year: 2023/2024

Group: K34212

Author: Titenko Elena Vitalevna

Lab: Lab3

Date of create: 1.03.2024

Date of finish: 3.03.2024

# Лабораторная работа №3 "Использование Asterisk в качестве SIP proxy"

### Цель
Изучить программный комплекс Asterisk. Настроить Asterisk для локальных звонков.

## Ход работы

### Asterisk

На Ubuntu установлен Asterisk:

![telegram-cloud-photo-size-2-5413641917255767596-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/ba24164f-0d78-4291-ba3d-7d4836623521)

Далее отредактированы файлы конфигурации.
Отредактирован файл sip.conf – добавлены два SIP-аккаунта и маршрутизация внутренних вызовов:

![telegram-cloud-photo-size-2-5413641917255767616-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/7c658df7-5b96-456c-9a40-7778d7e119e4)

![telegram-cloud-photo-size-2-5413641917255767615-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/176fa93b-1a7e-4274-ac3c-d0d4436f50c8)

А также файл extensions.conf:

![telegram-cloud-photo-size-2-5413641917255767623-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/7b775278-7684-4e05-bfcd-f339dc59f49b)

Необходимо перезапустить Asterisk, чтобы применить изменения. Проверен статус:

![telegram-cloud-photo-size-2-5413641917255767633-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/8a08f71e-c022-4ed5-8cf4-aff85cadfd3f)

Далее проверено, что аккаунты добавились:

![telegram-cloud-photo-size-2-5413641917255767636-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/7e18ae7a-69ab-47c2-bfde-a69f42e3a202)

### ZoiPer

С официального сайта было необходимо скачать ZoiPer5 – софт-телефон:

![telegram-cloud-photo-size-2-5413641917255767638-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/15b8fbfc-5a0d-48e8-8c9c-45537d2f195b)

Выполнен вход в один из созданных аккаунтов:

![telegram-cloud-photo-size-2-5413641917255767666-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/3deb4371-550c-4021-8b91-292105eb5984)

В качестве сервера указан локалхост:

![telegram-cloud-photo-size-2-5413641917255767668-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/579c1bba-d4b2-4513-ae77-bca9d068e1ae)

Теперь можно проверить, что порт для 1001 добавлен:

![telegram-cloud-photo-size-2-5413641917255767671-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/ee947996-7bd9-42c4-a6d6-f200b6404c72)

### MicroSIP

Для установки MicroSIP для начала нужно было поставить на машину wine:

![telegram-cloud-photo-size-2-5413641917255767683-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/880aaed7-cfe8-4861-b1d9-9d5d82ff9cec)

<img width="312" alt="image" src="https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/1bdb3eb0-d32b-43cd-8a9c-41beb2fc30d6">

Далее - непосредственно установка MicroSIP:

![telegram-cloud-photo-size-2-5413641917255767701-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/bde51fa3-0625-4dbe-bd77-90fa2d425d82)

![telegram-cloud-photo-size-2-5413641917255767704-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/40c28ff1-19ec-42ea-b923-1254d7fed3c0)

![telegram-cloud-photo-size-2-5413641917255767705-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/60ebc6ec-b769-42fa-8752-124f2c80df74)

В MicroSIP выполнен вход в аккаунт 1002 – введен пароль, адрес сервера, задано имя:

![telegram-cloud-photo-size-2-5413641917255767706-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/ab423e4c-1d46-4886-944f-8cfba3788cca)

Теперь и аккаунт 1002 получил тот же порт:

![telegram-cloud-photo-size-2-5413641917255767708-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/dcfcf514-7802-4a69-a5ca-8ca2fdee9592)

Теперь можно совершать звонки:

![telegram-cloud-photo-size-2-5413641917255767709-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/b8e07f57-04c8-4b60-814f-f6912e77b0de)

Успешно

![telegram-cloud-photo-size-2-5413641917255767710-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/36124dbe-b518-4de8-a1dc-a32f879942f4)

Можно также посмотреть историю вызовов:

![telegram-cloud-photo-size-2-5413641917255767711-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/6de1604a-bc7a-4a85-b08c-f1503f7539e0)

## Вывод

В ходе лабораторной работы изучены Asterisk, ZoiPer5, MicroSIP. Asterisk настроен для совершения локальных звонков. В результате успешно совершены звонки между двумя созданными аккаунтами.
