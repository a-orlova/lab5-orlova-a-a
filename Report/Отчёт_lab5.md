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
![image](https://github.com/user-attachments/assets/55a643eb-0b82-4f5d-99b6-e9776e156357)



**Работа с ветками**
1) Создаю новый текстовый файл README.md в терминале с помощью touch, а затем редактирую его в текстовом редакторе nano:
```bash
touch README.md
nano README.md
```
![image](https://github.com/user-attachments/assets/e3948e7d-7b50-4249-b724-68bb461bc4d7)

2) В терминале создаю и переключаюсь на новую ветку feature-login:
```bash
git checkout -b feature-login
```
3) Вношу изменения в файл с помощью nano:

![image](https://github.com/user-attachments/assets/4a4c4654-84fd-437f-9d7e-cd19b6cb9310)

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
![image](https://github.com/user-attachments/assets/9de4b96f-cc52-4b07-ae35-0ca0ec414490)

**Работа с удаленным репозиторием**

Переключаюсь на основную ветку, далее с помощью nano вношу изменения - добавляю название и меняю введение книги, коммит изменения и отправка всего на гитхаб.
```bash
git checkout main
nano README.md
git add README.md
git commit -m "Изменено название книги и введение"
git push origin main
```
![image](https://github.com/user-attachments/assets/228ed71c-ff39-4328-9781-f5b40719b79a)

**Моделирование конфликта**

Возвращаюсь в другую ветку и, подобно прошлым инструкциям, вношу там изменения в главе 2 - добавляю информацию о магии разрешения конфликтов
```bash
git checkout feature-login
git add README.md
git commit -m "Добавлен раздел о магии конфликтов"
git push origin feature-login
```
![image](https://github.com/user-attachments/assets/2a953932-f23c-4556-a737-a77![image](https://github.com/user-attachments/assets/212d450c-c708-49ac-a1fe-b18b944cd96e)
bdb34e561)

**Разрешение конфликта**

Когда я возвращаюсь в main ветку и хочу слить изменения, как и ожидается, возникает конфликт. 
```bash
git checkout main
git pull origin main
git merge feature-login
```
![image](https://github.com/user-attachments/assets/983a766c-5662-40bb-9aa0-7de57858b890)

Я открываю файл README.md и, удаляя лишнее, разрешаю конфликт.
Файл до изменений:

![image](https://github.com/user-attachments/assets/c6eb0e2f-ac4e-47e3-9fcf-6b983d3d0424)

Файл после изменений:

![image](https://github.com/user-attachments/assets/0de2ae71-98d5-4943-b5cb-16aa302c75a1)

Коммичу разрешение конфликта и отправьте изменения на гитхаб, как и раньше:

![image](https://github.com/user-attachments/assets/fb4e22ae-8782-40bb-a649-dbab327b5247)
