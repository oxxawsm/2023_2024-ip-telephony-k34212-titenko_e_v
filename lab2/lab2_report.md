University: ITMO University

Faculty: FICT

Course: IP-Telephony

Year: 2023/2024

Group: K34212

Author: Titenko Elena Vitalevna

Lab: Lab2

Date of create: 10.02.2024

Date of finished: 13.02.2024


# Лабораторная работа №2 "Конфигурация voip в среде Сisco Packet Tracer"

### Цель
Изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.

### Часть 1

Создана сеть, состоящая из маршрутизатора, коммутатора и ip-телефонов:

![telegram-cloud-photo-size-2-5350310077560641432-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/a3caa660-5df8-4255-a469-d398b61fba3c)

Изменено имя у маршрутизатора:

![telegram-cloud-photo-size-2-5350310077560641433-m](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/2dc7ab08-7e24-48bd-8db0-d6e1648e8695)

Далее настроен DHCP-сервер для передачи звонков и данных на роутер:

![telegram-cloud-photo-size-2-5355216596659984846-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/331b7a87-f252-4c2b-8867-df2481e1d08c)

Настройка Cisco CallManager Express на CMERouter:

![telegram-cloud-photo-size-2-5350310077560641446-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/b8c6f54d-e6cf-4157-9b51-31148a71913f)

Далее созданы VLAN порты на коммутаторе для взаимодействия коммутатора с маршрутизатором:

![telegram-cloud-photo-size-2-5350310077560641453-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/651e0f80-6759-47bc-8c32-d9b16af61143)

Далее настроены телефоны - им присвоены номера:

![telegram-cloud-photo-size-2-5350310077560641459-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/8b0a4cbb-d5de-4138-aa75-392518f2b496)

Теперь можно проверить звонки – они проходят успешно.

![telegram-cloud-photo-size-2-5350310077560641467-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/966bd3b2-517b-48a2-9087-0b5b64f012c5)

![telegram-cloud-photo-size-2-5350310077560641461-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/31060ded-9e26-44a0-9c87-66b5414c07cd)

![telegram-cloud-photo-size-2-5350310077560641462-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/9f3464f0-c488-4433-9111-450bbb047bb2)

### Часть 2

Созданная сеть дополнена ПК:

![telegram-cloud-photo-size-2-5350310077560641470-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/5f677fe1-11e2-4d53-8774-a610c47f1021)

Далее настроены VLAN порты на коммутаторе. vlan 99 смотрит на роутер, vlan 10 и 20 – на конечные устройства. Для маршрутизатора было решено использовать vlan 99, чтобы оставить диапазон под новые потенциальные конечные устройства.

![telegram-cloud-photo-size-2-5350310077560641476-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/743174b8-6b04-4bd6-8bab-c37654a3c771)

На маршрутизаторе созданы подынтерфейсы для vlan 10, 20 и 99:

![telegram-cloud-photo-size-2-5350310077560641486-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/60ece366-024c-4afc-9068-ee09f2824023)
![telegram-cloud-photo-size-2-5350310077560641487-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/e789e26b-0a68-4d44-af01-afc959c609ea)

А также прокинуты настройки для DHCP-сервера:

![telegram-cloud-photo-size-2-5350310077560641491-x](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/c2a353e8-dbb8-4640-a1e4-ef4dea2e8c1f)

Настроен телефонный сервис и номера телефонов.

Проверка связи между телефонами:

![telegram-cloud-photo-size-2-5350310077560641494-y](https://github.com/oxxawsm/2023_2024-ip-telephony-k34212-titenko_e_v/assets/63160594/9cf4a3b8-9c47-477e-ae19-fa71f9dba460)

## Вывод
В результате выполнения лабораторной работы с помощью Cisco Packet Tracer изучено построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.
