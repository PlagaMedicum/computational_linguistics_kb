# Computational linguistics knowledge base
База знаний проекта компьютерная лингвистика

### Содержание
1. [Начало](#intro)
2. [Установка OSTIS](#installation)
3. [Запуск OSTIS](#start)

### <a name="intro"></a> Начало
- Делаем себе копию базы(форкаем).
- Все понятия, над которыми хотим, начали или закончили работать храним на <b>Google Tab</b>: 
<https://docs.google.com/spreadsheets/d/18nNCC-Ydy1ah3_SeUuJ8MQDD3im1HLbOKU62bB0T5bw/edit?usp=drivesdk>

### <a name="installation"></a> Установка OSTIS
Рекомендуется ставить систему на Ubuntu версии 16.04, но установка на 18.04 здесь также рассматривается.
Открываем терминал.
Загружаем последние обновления системы
```sh
sudo apt-get update
```
Загружаем гит
```sh
sudo apt-get install git
```
Клонируем репозиторий с OSTIS'ом.
```sh
git clone https://github.com/ShunkevichDV/ostis
```
#### Для Ubuntu 16.04
```sh
cd ostis/scripts
./prepare.sh
```
Везде пишем "y", вводим пароль от кредитной карточки, ждём подтверждения.

#### Для Ubuntu 18.04
Скачиваем архивы по ссылке:
https://drive.google.com/open?id=1aF7rNgOWykf3TnyDlgnkeQ_sDGRZ2UAM

Распаковываем их в отдельные папки.
Заходим в папку libs и открываем в ней терминал и пишем:
```sh
sudo cp -R * /usr/lib
```
Заходим в папку bin и в ней выполняем команду:
```sh
sudo cp -R * ~/ostis/sc-machine/bin
```
Заходим в папку ostis/scripts и выполняем:
```sh
sudo ./prepare.sh
```
Соглашаемся на все предложения продать душу мэил.ру.

Если пишет, что не имеет прав доступа к каким-то файлам, прописываем:
```sh
chmod ugo+x ПутьКФайлу
```

Надеемся, что при запуске всё будет в норме...

### <a name="start"></a> Запуск OSTIS
Открываем терминал
```sh
cd ostis/scripts
```
#### Для Ubuntu 16.04
```sh
./restart_sctp.sh
```
Открываем новую вкладку (CTRL + SHIFT + T)
```sh
./run_scweb.sh
```
Открываем браузер и вводим адрес
```sh
localhost:8000
```
#### Для Ubuntu 18.04 
Делаем то же самое, но дописываем sudo в командах.
