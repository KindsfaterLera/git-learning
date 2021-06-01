1. Создать аккаунт на github

Существует давно.

2. Создать репозиторий

Средствами веб-интерфейса github создан репозиторий https://github.com/KindsfaterLera/git-learning.git

3. Создать локальный репозиторий

mkdir work
cd work
git init
git config --global user.name "Valeria Kindsfater"
git config --global user.email lera.kindsfater@gmail.com

4. Добавить несколько файлов

touch 1.txt
echo "Файл 1.txt создан"
touch 2.txt
echo "Файл 2.txt создан"

5. Создать в репозитории новую ветку

git branch new1

6. Пушить локальный репозиторий (все ветки) в github

Подключаем и именуем удаленный репозиторий 
git remote add origin https://github.com/KindsfaterLera/git-learning.git
Сохраняем логин и пароль (чтобы далеше не спрашивал)
git config credential.helper store
Выгружаем все ветки в удаленный репозиторий
git push origin --all

7. Клонировать удаленный репозиторий в новый локальный репозиторий

mkdir ../clone
cd ../clone
git init
git config --global user.name "Valeria Kindsfater (Clone)"
git config --global user.email lera.kindsfater@gmail.com
Загружаем все ветки из репозитория
git clone <репо>

8. Создать новую ветку и показать ветки

git branch new2
Посмотрим все локальные и удаленный ветки
git branch -a

9. Сделать 3 коммита

echo "Файл 1.txt изменен"
git commit -m  "Файл 1.txt изменен"

echo "Файл 2.txt изменен"
git commit -m  "Файл 2.txt изменен"

echo "Файл 1.txt изменен еще разщ"
git commit -m  "Файл 1.txt изменен еще раз"

10. Выгрузить в удаленный репозиторий

Подключаем и именуем удаленный репозиторий 
git remote add origin https://github.com/KindsfaterLera/git-learning.git
Выгружаем все ветки в удаленный репозиторий
git push origin --all

11. Внести изменения в файл, но не коммитить

echo "Файл 2.txt изменен еще раз. Коммитить не будем"

12. Показать разницу

git diff

13. При помощи git откатиться на прежнюю версию файла

git log
git reset --hard <id_коммита>

14. Слить новую ветку с master

git checkout master
git merge new2

15. Загрузить изменения

git add README.md
git commit -m "Добавлен файл README.md содержащий ход данной лабораторной работы"
git push origin --all

