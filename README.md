# Git Branch

Shramko_HW_GitHub_Group_28 

1. На локальном репозитории сделать ветки для:
- Postman 
  git branch Postman
- Jmeter 
  git branch Jmeter
- CheckLists
  git branch CheckLists
- Bag Reports
  git branch Bag_Reports
- SQL
  git branch SQL
- Charles
  git branch Charles
- Mobile testing
  git branch Mobile_testing

2. Запушить все ветки на внешний репозиторий: 
  - git push -u origin Postman
  - git push -u origin Jmeter
  - git push -u origin CheckLists
  - git push -u origin Bug_Reports
  - git push -u origin SQL
  - git push -u origin Charles
  - git push -u origin Mobile_testing

  либо перенести все измения на внешний репозиторий с помощью команды:
 - git push origin --all
  
- git branch -a для проверки наличия всех веток.
   В выведенном списке зеленым подсвеивается ветка, где мы находимся.

3. В ветке Bug Reports сделать текстовый документ со структурой баг репорта:
- git checkout Bag_Peports (в конце командной строки подсвечивается ветка, на которой мы находимся) 
- cat > Bag_report_structure

````
ID  
Summary
Project
Component
Version	
Severity:	
S1 (Blocker)
S2 (Critical)
S3 (Major)
S4 (Minor)
S5 (Trivial)

Priority:	
P1  (High)
P2  (Medium)
P3 (Low)

Status
Author
Assigned To
Workaround
Description
Steps to Reproduce
Result
Expected Result
Attachment

CTRL + C

```` 


4. Запушить структуру багрепорта на внешний репозиторий
- git status (проверяем файлы, которые могут быть добавлены на внешний репозиторий)
-  git add Bag_report_structure 
- git commit -m "add Bag_report_structure"
- git push

5. Вмержить ветку Bag Reports в Main:
- Для того, чтобы сделать merge ветки, необходимо находиться в ветке main
- git checkout main (в конце коммандной строки появляется название ветки)
- git merge Bag_Reports
   
   

6. Запушить main на внешний репозиторий: 
-   git checkout main
-   git add .
-  git commit -m "add all"
-  git push
  
7. В ветке CheckLists набросать структуру чек листа:
-   git checkout CheckLists (в конце командной строки подсвеччивается ветка)
-   cat > Checklists.txt
 
````
ID
Project 
Description
Status 
Equivalence classes
Priority
Verification
Result

   CTRL + C
````
8. Запушить структуру на внешний репозиторий:
-   git status (для просмотра измененных файлов, которые можно отправить на внешний репозиторий)
-   git add CheckLists.txt
-  git commit -m "add Checklists"
-   git push

9. На внешнем репозитории сделать Pull Request ветки CheckLists в main:
   1. В GitHub нажимаем на main репозиторий > нажимаем на branches > выбираем ветку Checklists и нажимаем на нее > нажимаем на Compare & Pull Request > base:main compare:Bag_Reports > Create pull request
   2. Либо, после переноса изменений ветки CheckLists во внешний репозиторий, заходим на GitHub >  открываем репозиторий main и можем увидеть сообщение "CheckLists had reecnt pushes 1 minute ago" > нажимаем на Campare & Pull request >  base: main compare: CheckLists > create a pull request> 
10. Синхронизировать Внешнюю и Локальную ветки Main: 
 -  git checkout main 
 - git pull 
