# kottans-frontend

## GIT

До цього вже мала поверхневе знайомство з Git, але більш звичайні "робочі" команди - clone, branch, push, merge. Не знала, що так багато інфи дає git log, а також про можливості cherry-pick i rebase.
В процесі пізнання
[terminal](https://www.dropbox.com/s/9gxw50hdxdmrg1c/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-07-22%20%D0%B2%2015.53.23.png?dl=0)
[https://learngitbranching.js.org/?locale=uk](https://www.dropbox.com/s/2vglbl7o9lzbkku/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-07-22%20%D0%B2%2018.11.59.png?dl=0)
[https://learngitbranching.js.org/?locale=uk](https://www.dropbox.com/s/y03fcetq5sun9r0/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-07-22%20%D0%B2%2021.45.19.png?dl=0)
Думаю можна попрактикуватися із застосуванням rebase замість merge

git init     --create a  repo

git clone URL  -- clone /copy a repo
  
git  status   --  check the  status /changes in repo

git  log -  to  review existing commits

with flags:
  --oneline  -- lists one commit per line -  SHA  first 7 numbers and commit message
  --stat  --to show the how many files were changed and the number of lines that were added/removed
  -p or  --patch    -- displays the files, location  and changes that have been modified
  -w   --  to ignore changes to whitespace

git show   --  shows a specific commit,  only one, can  be used with  the same flags as git log 

git add  --is used to move files from the Working Directory to the Staging Index

git rm --cashed   -- remove files from  the Staging Index

git commit -m "commit  message"   -   make  a commit  -takes files from the Staging Index and saves them in the repository

git diff   --to see changes that have been made but haven't been committed

git tag -a     --to  add a tag to a  specific commit (if SHA  used -  add to the last commit)
 
git branch   -- list out the branches in a repository

git branch name     --  create  a new  branch  named name 

git  branch -d  --to delete  branch


git checkout -b  -- to create a branch and switch to it all in one command.

git merge     --to combine branches in Git

git commit --amend  --to alter the most-recent commit

git revert <SHA-of-commit-to-revert>     -- to reverse a previously made commit

git reset   --to reset (erase) commits

git reset    -- to erase commit
with  flags 
 git reset --mixeg     --unstages committed changes
 git reset --soft     --moves committed changes to the staging index
 git reset --hard      --erase commits 

git  branch -f  main HEAD~3    -- насильно (force) переміщує  гілку  main на 3  предки (коміти) позад HEAD 

git cherry-pick main <SHA-commit>  --переміщає  вказаний коміт <SHA-commit> на main (  копіює новими комітами до поточного розташування)

git rebase -i  --  takes your entire feature branch and moves it to the tip of the main branch. It creates brand new commits for each commit in the original feature branch.

## Linux CLI, and HTTP

Курс про команди був на 100%  корисний,  я боялася команд раніше) і не вміла по суті нічого ними робити. Не знаю,  чи всі вони прямо  використовуються, проте  половина точно буде в роботі -  mkdir, cd, ls, cp, rm ... 

[quiz1](./task_linux_cli/quiz1.png)
[quiz2](./task_linux_cli/quiz2.png)
[quiz3](./task_linux_cli/quiz3.png)
[quiz4](./task_linux_cli/quiz4.png)

Мала  поняття про  структуру  URL ,  методи запитів та статус-коди, проте інформація  про  з'єднання та кешування  була  новою, раніше лише  чула про   це без  деталей. 
Здивувало, що  кешування  є таким механізмом,  що  сприяє  покращенню  ефективності  запит-відповідь.
В роботі здається  має  місце  використовуватися  практично все,  описане в статтях - від  структури  рядка до  кешування,  методи запитів + коди відповідей 
