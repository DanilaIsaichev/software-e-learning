---
title: "Установка офисного пакета Р7-Офис"
weight: 23
---

# Установка офисного пакета Р7-Офис

Р7-Офис - это российский офисный пакет, разрабатываемый компанией АО «Р7».

## Установка с использованием deb пакета

### Скачивание deb пакета

Для скачивания пакета нужно зайти на страницу загрузки Р7-Офис на официальном сайте: https://r7-office.ru/download_editor и нажать на кнопку скачивания deb пакета.

### Установка

Для установки Р7-Офис нужно:

1. Перейти к скаченному файлу и открыть его, щёлкнув по нему дважды левой кнопкой мыши.
2. В появившемся окне нажать «Установить пакет» и ввести пароль администратора.
3. После окончания процесса установки нажать «Применить».

## Установка с использованием репозитория

Для установки Р7-Офис с использованием официального репозитория необходимо использовать терминал.

### Запуск терминала

#### Astra Linux SE 1.7

1. перейти в меню «Пуск»;
2. открыть раздел «Системные»;
3. запустить терминал используя ярлык «Терминал fly».

#### Astra Linux SE 1.8

1. перейти в меню «Пуск»;
2. открыть раздел «Программы»;
3. перейти в раздел «Инструменты»;
4. запустить терминал используя ярлык «Konsole».

#### Сочетание клавиш

Также для запуска терминала во всех версиях Astra Linux можно использовать сочетание клавиш Win + T.

### Установка

Для установки пакета из репозитория необходимо установить ключи от этого репозитория. Для установки ключей выполним команду:

```bash
curl https://download.r7-office.ru/repos/RPM-GPG-KEY-R7-OFFICE.public | sudo gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/r7.gpg --import && sudo chmod 644 /etc/apt/trusted.gpg.d/r7.gpg
```

### Добавление репозитория в список

После установки ключей необходимо добавить репозиторий в список репозиториев. Сделаем это с помощью команды:

```bash
sudo echo 'deb https://downloads.r7-office.ru/repository/r7-desktop-apt/ buster main' | sudo tee /etc/apt/sources.list.d/r7.list
```

### Создание файла авторизации

После добавления репозитория нужно создать файл для авторизации в репозитории с помощью команды:

```bash
sudo nano /etc/apt/auth.conf.d/r7
```

В файл авторизации /etc/apt/auth.conf.d/r7.conf нужно записать следующие параметры:

```bash
machine downloads.r7-office.ru
login desktop
password gyxiLab84FByn7sCTd5JY
```

После чего нужно изменить параметры доступа к файлу /etc/apt/auth.conf.d/r7.conf с помощью команды:

```bash
sudo chmod 600 /etc/apt/auth.conf.d/r7.conf
```

Установка

Для установки пакета из добавленного репозитория нужно обновить список доступных пакетов с помощью команды:

```bash
sudo apt update
```

Установим Р7-Офис:

```bash
sudo apt-get install r7-office
```

## Запуск

После установки Р7-Офис будет доступен в разделе «Офис» меню «Пуск» (в случае, если используется Astra Linux SE 1.7) или в подразделе «Офис» раздела «Программы» меню «Пуск» (в случае, если используется Astra Linux SE 1.8).

## Активация

При первом запуске Р7-Офис появится уведомление «Вы используете пробную версию приложения».

Для активации Р7-Офис нужно зайти в раздел «О программе», нажать на кнопку «Загрузить файл лицензии» и выбрать файл лицензионного ключа.

# Анкетирование

<script src="https://forms.yandex.ru/_static/embed.js"></script><iframe src="https://forms.yandex.ru/u/6852ae7d068ff0673c3ab5fc?iframe=1" frameborder="0" name="ya-form-6852ae7d068ff0673c3ab5fc" width="650"></iframe>
