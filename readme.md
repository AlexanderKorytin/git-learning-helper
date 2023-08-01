# **Помощник по изучению Git**

---

## *Порядок команд в терминале по созданию локального репозитория:*

1. Переход в папку в которой необходимо создать репозиторий - cd /"путь к папке"
2. Создание репозитория - git init («Разгитить» папку, если что-то пошло не так, — rm -rf .git)
3. Проверка статуса - git status
4. Для добавления изменений в отсеивание - git add (--all or file name or . - для всей папки)
5. Для сохранения изменений - git commit -m "понятное описание изменения"

## *Привязка локального репозитория к удаленному на GitHub:*

1. Регистрируемся на GitHub по [ссылке](https://github.com "GitHub home") 
2. Переходим в Your repositories
3. Нажимаем кнопку New 
4. Вводим название репозитория без пробелов и нажимаем - создать
5. Копируем адрес SSH
6. Возвращаемся в терминал вводим команду - git remote add origin "ссылка SSH"
7. Для загрузки изменений в первый раз вводим команду - git push -u origin master (or main)
8. Далее -u опускаем

## *ХЭШ — идентификатор коммита:*

1. Вызывается командой git log
2. Git хеширует информацию о коммите с помощью алгоритма SHA-1 и получает для каждого коммита свой уникальный хеш
3. Обычно хеш — это короткая строка, которая состоит из цифр 0-9
0—9 и латинских букв A—F(неважно, заглавных или строчных)
4. Eсли хеш получить дважды для одного и того же набора входных данных, то результат будет гарантированно одинаковый

## *Git log:*

1. Получить сокращённый лог — git log --oneline, в терминале появятся только первые несколько символов хеша каждого коммита и их комментарии
2. Сокращённый хеш можно использовать точно так же, как и полный
3. если выход из просмотра логов не произошёл автоматически, нажмите клавишу Q

## *HEAD:*
1. Файл HEAD (англ. «голова», «головной») — один из служебных файлов папки .git. Он указывает на коммит, который сделан последним (то есть на самый новый)
2. Это синоним хеша последнего коммита — его можно передавать командам Git в качестве параметра
3. HEAD указывает на последний коммит. Если передать его в качестве параметра, Git поймёт вас

## *git status*

```mermaid
graph LR;
  untracked --"git add" --> staged;
  staged --"git commit"--> tracked;
  modified --"git add"-->staged;
  tracked --"Изменения"-->modified
```

## *Как читать git status:*

1. В итоге git status показывает только следующие состояния файлов:
 - staged (Changes to be committed в выводе git status)
 - modified (Changes not staged for commit)
 - untracked (Untracked files)

## *Оформление сообщений к коммитам:*

1. Хорошо, когда:
 - сообщение коммита легко читается
 - оно информативное
 - все сообщения оформлены в одном стиле


