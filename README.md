## Branch

1. На локальном репозитории сделать ветки для: Postman, Jmeter, CheckLists, Bug Reports, SQL, Charles, Mobile testing.
 
`git branch Postman` \
`git branch Jmeter` \
`git branch CheckLists` \
`git branch Bug_Reports` \
`git branch SQL` \
`git branch Charles` \
`git branch Mobile_Testing`


2. Запушить все ветки на внешний репозиторий \
`git push --all -u origin`
 
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта. \
`git checkout Bug_Reports` - переход в данную ветку \
`vim bug_report.txt` - создание файла и ввод следующей информации:
```
Структура баг-репорта.
1. Краткое описание проблемы (Summary)
2. Проект (Project)
3. Компонент приложения (Component). Название части функции тестируемого продукта
4. Номер версии, на которой найдена ошибка (Version)
5. Серьезность (Severity) 
- Blocker
- Critical
- Major
- Minor
- Trivial
6. Приоритет (Priority)
- High
- Medium 
- Low
7. Статус (Status). Статус бага в его жизненном цикле
8. Автор (Author). Создатель баг-репорта
9. Назначен на (Assigned To)
10. Окружение (Environment). Оперционная система, версия браузера и т.д.
11. Шаги воспроизведения (Steps to Repruduce)
12. Фактический результат.(Actual Result)
13. Ожидаемый результат (Expected Result)
14. Приложения. Скриншоты, документы, видео, логи и т.д.
```
- `:wq` - выход и сохранение

4. Запушить структуру багрепорта на внешний репозиторий. \
`git add bug_report.txt` \
`git commit -m "add bug_report.txt"` \
`git push`

5. Вмержить ветку Bag Reports в Main. \
`git checkout main` - переход в ветку main \
`git merge Bug_Reports` 

6. Запушить main на внешний репозиторий. \
`git push -u origin main`

7. В ветке CheckLists набросать структуру чек листа. \
`git checkout CheckLists` \
`vim checklist.txt`- создание файла и ввод следующей информации:

```
Стандартные атрибуты:

1. Название проекта.
2. Наименование проверки. (краткое описание сути теста)
3. Ожидаемый результат. (НЕ обязательный пункт)
4. Статус. (Passed- проверка пройдена успешно.
             Falied - найден баг. 
	     Blocked- невозможно проверить, т.к баг блокирует проверку.
	     In progress- в процессе работы тестировщика. 
	     Not run- еще не проверено.
	     Skipped- не будет проверяться по какой-либо причине. Например, фукционал еще не реализован.)
```
 - `:wq` - выход и сохранение
 
8. Запушить структуру на внешний репозиторий. \
`git add . ` \
`git commit -m "add cheklist.txt"` \
`git push`

9. На внешнем репозитории сделать Pull Request ветки CheckLists в main.
- Данное действие производится во вкладке `Pull request`.

10. Синхронизировать Внешнюю и Локальную ветки Main. \
`git checkout main` \
`git pull`
