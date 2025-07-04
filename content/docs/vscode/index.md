---
title: "Установка редактора кода Visual Studio Code"
weight: 55
---

# Установка редактора кода Visual Studio Code

Visual Studio Code - это проприетарная версия редактора Code, разрабатываемого компанией Microsoft.

## Установка с использованием deb пакета

### Скачивание deb пакета

Для скачивания пакета нужно зайти на страницу загрузки Visual Studio Code на официальном сайте: https://code.visualstudio.com/download и нажать на кнопку скачивания deb пакета.

### Установка

Для установки Visual Studio Code нужно:
1. Перейти к скаченному файлу и открыть его, щёлкнув по нему дважды левой кнопкой мыши.
2. В появившемся окне нажать «Установить пакет» и ввести пароль администратора.
3. После окончания процесса установки нажать «Применить».

### Последующие обновления

В процессе установки пакета в список репозиториев будет добавлен репозиторий Visual Studio Code, благодаря чему обновления можно будет устанавливать с помощью менеджера пакетов Synaptic или через терминал.

## Установка с использованием репозитория

Для установки Visual Studio Code с использованием официального репозитория необходимо использовать терминал.

### Запуск терминала

#### Astra Linux SE 1.7

1) перейти в меню «Пуск»;
2) открыть раздел «Системные»;
3) запустить терминал используя ярлык «Терминал fly».

#### Astra Linux SE 1.8

1) перейти в меню «Пуск»;
2) открыть раздел «Программы»;
3) перейти в раздел «Инструменты»;
4) запустить терминал используя ярлык «Konsole».

#### Сочетание клавиш

Также для запуска терминала во всех версиях Astra Linux можно использовать сочетание клавиш Win + T.

### Установка ключей репозитория

Для установки пакета из репозитория необходимо установить ключи от этого репозитория. Для установки ключей выполним команду:

```bash
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor | sudo dd of=/etc/apt/keyrings/packages.microsoft.gpg
```

### Добавление репозитория в список

После установки ключей необходимо добавить репозиторий в список репозиториев. Сделаем это с помощью команды:

```bash
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" | sudo tee /etc/apt/sources.list.d/vscode.list
```

### Установка

Для установки пакета из добавленного репозитория нужно обновить список доступных пакетов с помощью команды:

```bash
sudo apt update
```

Установим Visual Studio Code:

```bash
sudo apt install code
```

## Запуск Visual Studio Code

После установки Visual Studio Code будет доступен в разделе «Разработка» меню «Пуск» (в случае, если используется Astra Linux SE 1.7) или в подразделе «Инструменты» раздела «Программы» меню «Пуск» (в случае, если используется Astra Linux SE 1.8)

# Анкетирование

<script src="https://forms.yandex.ru/_static/embed.js"></script><iframe src="https://forms.yandex.ru/u/6852b075f47e73681b5a249b?iframe=1" frameborder="0" name="ya-form-6852b075f47e73681b5a249b" width="650"></iframe>
