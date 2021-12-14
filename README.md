# git-commands
базовые команды <br>
git clone адрес репозитория - клонировать репозиторий на локальный компютер <br>
git commit -m 'initial commit' комит изменений в локальный репозиторий <br>
git push -u origin master - только первый раз отправка изменений в удаленный репозиторий <br>
git push - все последующие разы отправка изменений в удаленный репозиторий <br>
<br>
<br>
окат изменений <br>
git pull - скачивается актуальная версия удаленного репозитория и все изменения применяются к локальному репозиторию <br>
git pull origin - подтягивает с основной ветки все комиты <br>
git reset --hard отменяет git pull <br>
checkout - перейти в другую ветку <br>
discard - не отправлять в репозиторий те изменения которые нам не нравятся <br>
revert - откатить существующие комиты <br>
hard reset -откатить целую пачку комитов <br>
<br>
<br>
работа с ветками <br>
merge - сначала подтягиваем в свою ветку из master все изменения <br>
merge - потом тестируем и делаем слияние переходим (checkout) в master и применяем (merge) все изменения из нашей ветки <br>
<br>
<br>
git commit -a -m 'commit all edited files' закомитить все измененные файлы безиспользования команды git add <br>
git clone - скачивание репозитория <br>
git status - просмотр текущих изменений <br>
git add - добавить файл в локальный репозиторий <br>
git commit - коммит в локальный репозиторий <br>
git push - коммит в удаленный репозиторий <br>
<br>
<br>
В консольном git можно указать настройки сетевого подключения. Прокси, порты, аутентификацию. <br>
git config --global http.proxy http://proxyuser:proxypwd@proxy.server.com:8080  <br>
(указываем ваши креденшлс, если есть, прокси-сервер и порт) <br>
<br>
<br>
Работа с ветками <br>
git branch -a  посмотреть в какой ветке мы находимся и показать все ветки ключ -а   all <br>
git branch newbranch  - создать новую ветку с именем newbranch <br>
git checkout newbranch - перейти в новую ветку <br>
git push origin newbranch -  (сначала переключиться на мастер) отправить в удаленный репозиторий ветку newbranch <br>
git branch -d newbranch - удалить ветку newbranch из локального репозитория  <br>
git push origin --delete newbranch - удалить ветку newbranch в удаленном репозитории <br>
<br>
<br>
Посмотреть настройки Git <br>
git config --list - показывает имя и все данные глобально <br>
<br>
<br>
Работа с версиями программы <br>
1. Разработку лучше вести не в ветке master, <br>
   а в другой ветке, например, develop, новые функции программы ветвить от develop, <br> 
   тестить и фиксить в develop, и только когда код отлажен до какой-то стабильной версии программы,  <br>
   сливать изменения в master. <br>
2. При этом удобно добавить тэг с номером версии и изменениями что допилили в этой версии (release notes). <br>
3. По тэгу легко найти нужную версию в логе, <br>
   и можно по этому коммиту (вообще можно по любому коммиту) <br>
   воссоздать в отдельной ветке состояние программы в этой версии. <br>
   <br>
   <br>
api/get-temperature-value <br>
feature/select2-ibrary-added <br>
fix/incorrect-users-sorting-fixed <br>
т.е. принцип: "чем является доработка" / "что именно доработано". <br>
