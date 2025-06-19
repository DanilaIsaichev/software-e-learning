---
title: "Установка редактора кода VSCodium"
weight: 54
---

# Установка редактора кода VSCodium

VSCoduim - это свободная поддерживаемая сообществом версия редактора Code, разрабатываемого компанией Microsoft.

## Установка с использованием репозитория

Для установки VSCoduim с использованием официального репозитория необходимо использовать терминал.

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
curl https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/raw/master/pub.gpg | gpg --dearmor | sudo dd of=/usr/share/keyrings/vscodium-archive-keyring.gpg
```

### Добавление репозитория в список

После установки ключей необходимо добавить репозиторий в список репозиториев. Сделаем это с помощью команды:

```bash
echo "deb [arch=amd64,arm64 signed-by=/usr/share/keyrings/vscodium-archive-keyring.gpg] https://download.vscodium.com/debs vscodium main" | sudo tee /etc/apt/sources.list.d/vscodium.list
```

### Установка

Для установки пакета из добавленного репозитория нужно обновить список доступных пакетов с помощью команды:

```bash
sudo apt update
```

Установим VSCodium:

```bash
sudo apt install codium
```

## Запуск VSCodium

После установки VSCodium будет доступен в разделе «Утилиты» меню «Пуск» (в случае, если используется Astra Linux SE 1.7) или в подразделе «Офис» раздела «Программы» меню «Пуск» (в случае, если используется Astra Linux SE 1.8)

# Анкетирование

<script src="https://forms.yandex.ru/_static/embed.js"></script><iframe src="https://forms.yandex.ru/u/6852b02384227c677065216f?iframe=1" frameborder="0" name="ya-form-6852b02384227c677065216f" width="650"></iframe>
