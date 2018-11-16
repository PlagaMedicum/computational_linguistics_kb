# Computational linguistics knowledge base
База знаний проекта компьютерная лингвистика

### Содержание
1. [Инструкция по созданию своей копии базы](#instruction)
2. [Установка системы](#installing)
3. [Запуск системы](#start)
4. [Клонирование базы (ТОЛЬКО НА ПУСТОЙ OSTIS)](#cloning)
5. [Отправка изменений (с ветки master)](#pushing)
6. [Получение изменений](#pulling)
7. [Основные ссылки](#links)

### <a name="instruction"></a> Инструкция по созданию своей копии базы
- Вилкануть себе репозиторий (вверху есть кнопка Fork)

### <a name="installing"></a> Установка системы
Установка осуществляется с системы ubuntu через терминал
```sh
git clone https://github.com/ShunkevichDV/ostis здесьМожноВвестиСвоеНазваниеДляПапкиСистемы
```
Если не ввести название папки, то она будет называться ostis
```sh
cd ostis/scripts
./prepare.sh
```
Если что-то спросит, то соглашаемся, вводим пароль, когда запросит и т.д.

### <a name="start"></a> Запуск системы
Открываем терминал
```sh
cd ostis/scripts
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

### <a name="cloning"></a> Клонирование базы (ТОЛЬКО НА ПУСТОЙ OSTIS)
Открываем терминал
```sh
cd ostis
```
ВНИМАНИЕ!!! Следующая команда удалит папку kb (совсем, полностью, без возможности восстановления, но вы и так должны это знать)
```sh
rm -f -R  kb
git clone ссылкаНаВашуКопиюРепозитория kb
cd kb
git remote add mainRepository https://github.com/PlagaMedicum/computational_linguistics_kb
git fetch mainRepository
git checkout -b main mainRepository/master
git checkout master

```

### <a name="pushing"></a> Отправка изменений (с ветки master)
- Закоммитить и залить на свой репозиторий локальные изменения
```sh
git add .
git commit -m "commit description"
git push
```
- Рекомендуется ознакомиться с [данной](https://htmlacademy.ru/blog/27-how-to-squash-commits-and-why-it-is-needed) статьёй: много маленьких коммитов это, конечно, хорошо, но склеивайте хотя бы такие коммиты, как:
> Merge pull request
> Merge remote-tracking branch 'upstream/master' 
- Создать пуллреквест c комментарием в формате: 
> [Имя Фамилия] Комментарий.
- Отметить в [Google Tab]

### <a name="pulling"></a> Получение изменений
- Изменения на ветке master должны быть закомичены и, желательно, приняты мной
```sh
git checkout main
git pull
git checkout master
git merge main
```

### <a name="links"></a> Основные ссылки
- [Google Tab]


   [Google Tab]: <https://vk.com/away.php?to=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F18nNCC-Ydy1ah3_SeUuJ8MQDD3im1HLbOKU62bB0T5bw%2Fedit%3Fusp%3Ddrivesdk&cc_key=>
   [OSTIS]: <https://github.com/ShunkevichDV/ostis>
   [База Знаний IMS]: <https://github.com/ShunkevichDV/ims.ostis.kb>
