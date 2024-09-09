# ЛАБ 5
**Введение**

1) В первую очередь создаю репозиторий на гитхабе: вхожу в свою учетную запись, нажимаю на кнопку New Repository, ввожу имя репозитория - git-practice, делаю его публичным. Затем копирую его URL.
![image](https://github.com/user-attachments/assets/7cd220c1-1d33-4461-ad64-f357389e0ce3)
![image](https://github.com/user-attachments/assets/fffb4837-1e71-45f5-99e5-16d496badae2)
2) Теперь клонирую репозиторий. Ввожу команду:
```bash
git clone git@github.com:a-orlova/git-practice.git
```
Затем перехожу в этот репозиторий с помощью команды cd
```bash
cd git-practice
```
3) Добавляю внутри репозитория текстовый файл example.txt и сразу добавляю туда текст - структуру книги с помощью команды echo: 
```bash
echo "Глава 1: Введение\nГлава 2: Основная часть" > example.txt
```
Добавляю файл в те, которые будут отслеживаться с помощью:
```bash
git add example.txt
```
Делаю коммит с сообщением:
```bash
git commit -m "File added example.txt"
```
Отправляю изменения в удаленный репозиторий:
```bash
git push origin main
```
4) Создаю новую ветку и переключаюсь на неё:
```bash
git branch feature-branch
git checkout feature-branch
```
5) Редактирую файл example.txt, добавив новый текст с помощью команды echo:
```bash
echo "Глава 3: Заключение" >> example.txt
```
Сохраняю файл и добавляю его в гит:
```bash
git add example.txt
```
Делаю новый коммит:
```bash
git commit -m "Added conclusion to example.txt"
```
Отправляю изменения:
```bash
git push origin feature-branch
```
6) Теперь занимаюсь сливанием изменений. Переключаюсь обратно на основную ветку:
```bash
git checkout main
```
Далее выполняю слияние ветки feature-branch в основную ветку:
```bash
git merge feature-branch
```
Отправляю объединенные изменения на GitHub:
```bash
git push origin main
```
7) Проверяю, что файл изменен верно, и все ветки слиты. Все верно!
![image](https://github.com/user-attachments/assets/e8c73438-c427-4e54-9a0f-40a16381c788)
![image](https://github.com/user-attachments/assets/587728c4-2560-4dd6-824d-8a9001849816)

**Работа с ветками**
1) Создаю новый текстовый файл NewFile.md прямо на сайте, добавляю туда нужный текст.
![image](https://github.com/user-attachments/assets/f9c9bab5-ce2b-4121-96c5-cf15ec46e102)
![image](https://github.com/user-attachments/assets/30ae1bbb-3ce0-43b8-a38f-5c9b360887ee)

2) В терминале создаю и переключаюсь на новую ветку feature-login:
```bash
git checkout -b feature-login
```
3) Вношу изменения в файл с помощью echo:
```bash
echo " " >> NewFile.md
echo "## Глава 3: Вход в систему" >> NewFile.md
echo "Раздел по новой функциональности входа в систему." >> NewFile.md
```
4) Добавляю файл для отслеживания изменений:
```bash
git add README.md
```
Создаю коммит с сообщением:
```bash
git commit -m "Добавлена глава 3: Вход в систему"
```
Отправляю изменения в ветку feature-login на GitHub:
```bash
git push origin feature-login
```
![image](https://github.com/user-attachments/assets/d66be7fb-7141-4547-9a8d-cb78a8ccc5aa)

**Работа с удаленным репозиторием**
1) 
