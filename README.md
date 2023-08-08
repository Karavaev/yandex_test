# Шпаргалка Git
## Проверка установки Git
```
$ git --version
git version x.xx.x #вывод сообщения при наличии в системе git
```
## Настройки .gitconfig

Настраиваем git иначе будут выдаваться подсказки об отсутствии данных пользователя

```
$ git config --global user.name "User Namovich" 
# имя или ник нужно написать латиницей и в кавычках

$ git config --global user.email username@yandex.ru
# здесь нужно указать свой настоящий email 
```
Для проверки вводим 

```
$ git config --list 
```

## Инициализируем репозиторий

Создаем папку для проекта, переходим в нее и инициализируем проект.

```
$ mkdir yandex_git && cd yandex_git && git init
```

## Добавляем файлы в репозиторий

Подготавливаем необходимые файлы к коммиту.
Проверяем изменения командой 

```
$ git status
```
Если изменяемые файлы удовлетворяют, добавляем их 

```
$ git add XXX.XXX #отдельно файл
$ git add --all # подготовили к сохранению все файлы в репозитории
```

## Делаем коммит

Сохраняем изменения с информативным сообщением о изменениях.

```
$ git commit -m 'Создания тестового проекта' 
```

## Просматриваем историю коммитов

```
$ git log
```

## Удаленный репозиторий 

Gitea — это легкая платформа DevOps. Он позволяет командам и разработчикам выполнять высокоэффективные и простые операции от планирования до производства.

## Связываем локальный и удалённый репозитории

При создании в веб-интерфейсе репозитория получаем подсказку привязки и синхронизации. Команды используются для нового репозитория. 


```
$ git remote add origin https://gitea.xxxx.ru/xxxx/yandex_git.git
$ git push -u origin master
```
