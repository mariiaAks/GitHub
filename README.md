# GitHub
GitHub. HW_2

Предусловия:
1. В веб интерфейсе github создан внешний репозиторий: create new repository GitHub --public
2. Репозиторий GitHub клонирован на локальный компьютер.
   $ git clone git@github.com:mariiaAks/GitHub.git
3. $cd GitHub

Задание:

1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing

      $git branch Postman
      $git branch Jmeter
      $git branch CheckLists
      $git branch Bag_Reports
      $git branch SQL
      $git branch Charles
      $git branch Mobile_testing

2. Запушить все ветки на внешний репозиторий

        $git push -u origin Postman
        $git push -u origin Jmeter
        $git push -u origin CheckLists
        $git push -u origin Bag_Reports
        $git push -u origin SQL
        $git push -u origin Charles
        $git push -u origin Mobile_testing

3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта

        $git checkout Bag_Reports
        $cat > bug_report.txt

        Bug_id: 
        Title: 
        Severity: 
        Priority: 
        Summary: 
        Precondition: 
      	  1) 
      	  2) 
        StepToReproduce: 
          1) 
      	  2) 
      	  3)
        Environment: 
        ExpectedResult: 
        ActualResult: 
        Attachments: 

        Ctrl+C

4. Запушить структуру багрепорта на внешний репозиторий

        $git add .
        $git commit -m "Add new file bug_report.txt"
        $git push

5. Вмержить ветку Bag Reports в Main

        $git checkout main
        $git merge Bag_Reports -m "merge Bag_Reports"

6. Запушить main на внешний репозиторий.

        $git push

7. В ветке CheckLists набросать структуру чек листа.

        $git checkout CheckLists
        $cat > checkLists.txt

        Id: 
        Description: 
        Environment:  
        Status: 
        Link to bug_report: 

        Ctrl+C

8. Запушить структуру на внешний репозиторий

        $git add .
        $git commit -m "Add new file checkLists.txt"  
        $git push

9. На внешнем репозитории сделать Pull Request ветки CheckLists в main

        Нажать Pull Requests
        Нажать Compare & pull request (CheckLists had recent pushes 1 minute ago)
        Нажать Create pull request
        Нажать Merge pull request
        Нажать Confirm merge

10. Синхронизировать Внешнюю и Локальную ветки Main

        $git checkout main
        $git fetch
        $git pull
