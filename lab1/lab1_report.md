University: ITMO University

Faculty: FICT

Course: IP-Telephony

Year: 2023/2024

Group: K34212

Author: Titenko Elena Vitalevna

Lab: Lab1

Date of create: 10.02.2024

Date of finished: 13.02.2024

# Лабораторная работа №1 "Базовая настройка ip-телефонов в среде Сisco packet tracer"

### Цель
Изучить рабочую среду Cisco Packet Tracer, ознакомиться с интерфейсами основных устройств, типами кабелей, научиться собирать топологию. Изучить построение сети IP-телефонии с помощью маршрутизатора, коммутатора и IP телефонов Cisco 7960 в среде Packet tracer

### Часть 1

Создана схема сети, состоящая из 4-х коммутаторов и подключенных к ним устройствам (ПК): 

![telegram-cloud-photo-size-2-5350310077560641364-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/01291a0b-8ddb-4da9-b435-34ffc919a39b)

Каждому ПК в созданной сети присвоен адрес из сети 192.168.0.0/24 следующим образом:

![telegram-cloud-photo-size-2-5350310077560641367-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/1c3893ae-3afc-4088-9d6a-8cd83ab90aba)

После этой базовой настройки компьютеры уже могут друг с другом пинговаться. Коммутатору дополнительная настройка не требуется.

Примеры пингов:

![telegram-cloud-photo-size-2-5350310077560641374-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/d4acfad5-8c5c-4213-a76b-6301fabcf3f8)

### Часть 2

В этой части работы создана еще одна схема: маршрутизатор, коммутатор и 2 ip-телефона:

![telegram-cloud-photo-size-2-5350310077560641379-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/4e5bf2ec-a375-45fb-80d2-207ff6a10fa7)

Телефоны нужно включить, присоединив адаптер питания в графическом интерфейсе устройств:

![telegram-cloud-photo-size-2-5350310077560641380-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/b50f4d4b-2179-43c2-82e0-3ba36a48e8eb)

![telegram-cloud-photo-size-2-5350310077560641381-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/deb0531a-7163-4def-bfa5-4c3921c5a3ba)

Теперь можно продолжать настройку сети.

Изменено имя роутера:

![telegram-cloud-photo-size-2-5350310077560641383-m](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/81298864-c6cf-4d05-9351-02885bf7a86b)

Далее интерфейсу маршрутизатора, смотрящему на коммутатор назначен ip-адрес и маска подсети:

![telegram-cloud-photo-size-2-5350310077560641385-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/cdf23091-bf72-40ce-933c-2b714cc6a680)

Далее создан DHCP-пул phones с адресами из сети 192.168.0.0 (адрес роутера не учитывается). Также маршрутизатор из нашей сети назначен маршрутизатором по умолчанию для созданного DHCP-пула. Включена опция 150: с помощью этой функциональности телефоны получают адрес маршрутизатора, на котором хранится образ операционной системы для них.

![telegram-cloud-photo-size-2-5350310077560641388-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/47597c8f-b79e-44dc-89f0-fa47c0457519)

Создан сервис ip-телефонии. Адреса для телефонов выдаются с маршрутизатора по умолчанию:

![telegram-cloud-photo-size-2-5350310077560641390-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/22442974-a0d1-4270-b828-1cf81390ed67)

Далее на коммутаторе включена поддержка VoIP-интерфейсов:

![telegram-cloud-photo-size-2-5350310077560641392-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/9f5cd0d1-a5c7-46b8-81eb-8573385c1b1d)

Первому телефону в сети задан номер 111, а второму - 222:

![telegram-cloud-photo-size-2-5350310077560641413-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/16c4931b-3a7f-4f3f-b98f-7250c9f61e60)

Теперь телефоны должны друг друга видеть. В графическом интерфейсе букально можно позвонить с одного на другой, при этом услышать характерный звук звонка:

![telegram-cloud-photo-size-2-5350310077560641410-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/0933c97c-0724-416c-9ffc-9ee8fba23b75)

## Вывод

В ходе выполнения лабораторной работы изучено построение сети IP-телефонии с помощью маршрутизатора, коммутатора и IP телефонов Cisco 7960 в среде Packet tracer.
Созданы и настроены две схемы сети в CPT – 1) сеть, состоящая из коммутаторов и ПК, 2) сеть, состоящая из ip-телефонов, маршрутизатора и коммутатора. В результате освоены базовые принципы работы ip-телефонии на примере настройки ip-телефонов Cisco.
