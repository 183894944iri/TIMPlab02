# TIMPlab02
### 1 PART
   1. Создаю пустой репозиторий на github.com под названием "TIMPlab02"
   2. mkdir TIMPlab02       
   3. cd TIMPlab02
   4. echo "# TIMPlab02" >> README.md
   5. git init
   6. git add README.md
   7. git commit -m "first commit"
   8. git branch -M main
   9. git remote add origin https://github.com/183894944iri/TIMPlab02.git
   10. git pull --rebase origin main
   11. git push origin main
   12. Реализовываю программу с плохим стилем кода cat > "Hello world.cpp" << EOF
   13. > <img width="307" alt="image" src="https://github.com/183894944iri/TIMPlab02/assets/113174903/cdcb60a1-ba17-4490-8732-687793e78b56">
   14. git add "Hello world.cpp"
   15. git commit -m "added new cpp file" 
   16.  Вызываю редактор nano sudo nano "Hello world.cpp"
   17.  Меняю код программы 
   18. > <img width="420" alt="image" src="https://github.com/183894944iri/TIMPlab02/assets/113174903/f82524e5-407d-4a1d-8eb8-7e658a811706">
   19.  git commit -a -m "changed cpp file" 
   20.  git push -u origin main 
### 2 PART
1. git checkout -b patch1
2. nano "Hello world.cpp"
3. Меняю код программы
4. > <img width="500" alt="image" src="https://github.com/183894944iri/TIMPlab02/assets/113174903/0acc2f75-aba8-4c98-a9c0-4b026a129f45">
5. git commit -a -m "fixed cpp file"
6. git push -u origin patch1
7. Создаю pull-request `patch1 -> main`
8. nano "Hello world.cpp"
9. Добавляю в код комментарии 
10. > <img width="511" alt="image" src="https://github.com/183894944iri/TIMPlab02/assets/113174903/a60a7647-c053-4f12-8fa0-19c4df53381b">
11. git commit -a -m "added comments"
12. git push -u origin patch1
13. Произвожу слияние `patch1 -> main` и удаляю ветку `patch1` в удаленном репозитории
14. git checkout main
15. git pull origin main
16. git log
17. > <img width="528" alt="image" src="https://github.com/183894944iri/TIMPlab02/assets/113174903/9f0a5120-b025-4555-b931-aae09f04dfe0">
18. git branch -d patch1
### 3 PART
1. git checkout -b patch2
2. Изменяю *code-style* с помощью утилиты clang-format  
 > clang-format -i -style=Mozilla "Hello world.cpp"
3. git commit -a -m "changed code style in cpp file"
4. git push -u origin patch2 
5. Создаю pull-request `patch2 -> main`
6. В ветке `main` меняю комментарии
7. В pull-request появились конфликты
8. git pull origin main --rebase
9. nano "Hello world.cpp"
> руками объединила файлы
10. git rebase --continue
11. git push -f origin patch2
> конфликты пропали
12. Merge pull-request `patch2 -> main`
