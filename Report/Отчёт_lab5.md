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
3) Добавляю внутри репозитория текстовый файл example.txt и сразу добавляю туда текст-пример с помощью команды echo: 
```bash
echo "Это текст для примера" > example.txt
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
echo "Изменение файла" >> example.txt
```
Сохраняю файл и добавляю его в гит:
```bash
git add example.txt
```
Делаю новый коммит:
```bash
git commit -m "Updated example.txt with new text"
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
![image](https://github.com/user-attachments/assets/9148e6b6-661d-4d2f-be8d-3cb711e23fec)
![image](https://github.com/user-attachments/assets/5d869a9b-0bbe-47fd-8a26-e935715c5b1d)

7) Проверяю, что файл изменен верно, и все ветки слиты. Все верно!
![image](https://github.com/user-attachments/assets/d015ed15-c4d6-40da-a6b6-d9d027f856e9)
![image](https://github.com/user-attachments/assets/c6d2acd1-e20c-471b-9efc-6fd9628b3ceb)


**Работа с ветками**
1) Создаю новый текстовый файл README.md в терминале с помощью touch, а затем редактирую его в текстовом редакторе nano:
```bash
touch README.md
nano README.md
```
2) В терминале создаю и переключаюсь на новую ветку feature-login:
```bash
git checkout -b feature-login
```
3) Вношу изменения в файл с помощью nano:

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
![image](https://github.com/user-attachments/assets/f73b6457-5d6a-4683-a8dc-19cc4551561a)


**Работа с удаленным репозиторием**
1) 

