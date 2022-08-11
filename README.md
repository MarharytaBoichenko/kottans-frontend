# kottans-frontend

## GIT

До цього вже мала поверхневе знайомство з Git, але більш звичайні "робочі" команди - clone, branch, push, merge. Не знала, що так багато інфи дає git log, а також про можливості cherry-pick i rebase.
В процесі пізнання
[terminal](https://www.dropbox.com/s/9gxw50hdxdmrg1c/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-07-22%20%D0%B2%2015.53.23.png?dl=0)
[https://learngitbranching.js.org/?locale=uk](https://www.dropbox.com/s/2vglbl7o9lzbkku/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-07-22%20%D0%B2%2018.11.59.png?dl=0)
[https://learngitbranching.js.org/?locale=uk](https://www.dropbox.com/s/y03fcetq5sun9r0/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-07-22%20%D0%B2%2021.45.19.png?dl=0)
Думаю можна попрактикуватися із застосуванням rebase замість merge

git init --create a repo

git clone URL -- clone /copy a repo

git status -- check the status /changes in repo

git log - to review existing commits

with flags:
--oneline -- lists one commit per line - SHA first 7 numbers and commit message
--stat --to show the how many files were changed and the number of lines that were added/removed
-p or --patch -- displays the files, location and changes that have been modified
-w -- to ignore changes to whitespace

git show -- shows a specific commit, only one, can be used with the same flags as git log

git add --is used to move files from the Working Directory to the Staging Index

git rm --cashed -- remove files from the Staging Index

git commit -m "commit message" - make a commit -takes files from the Staging Index and saves them in the repository

git diff --to see changes that have been made but haven't been committed

git tag -a --to add a tag to a specific commit (if SHA used - add to the last commit)

git branch -- list out the branches in a repository

git branch name -- create a new branch named name

git branch -d --to delete branch

git checkout -b -- to create a branch and switch to it all in one command.

git merge --to combine branches in Git

git commit --amend --to alter the most-recent commit

git revert <SHA-of-commit-to-revert> -- to reverse a previously made commit

git reset --to reset (erase) commits

git reset -- to erase commit
with flags
git reset --mixeg --unstages committed changes
git reset --soft --moves committed changes to the staging index
git reset --hard --erase commits

git branch -f main HEAD~3 -- насильно (force) переміщує гілку main на 3 предки (коміти) позад HEAD

git cherry-pick main <SHA-commit> --переміщає вказаний коміт <SHA-commit> на main ( копіює новими комітами до поточного розташування)

git rebase -i -- takes your entire feature branch and moves it to the tip of the main branch. It creates brand new commits for each commit in the original feature branch.

## Linux CLI, and HTTP

Курс про команди був на 100% корисний, я боялася команд раніше) і не вміла по суті нічого ними робити. Не знаю, чи всі вони прямо використовуються, проте половина точно буде в роботі - mkdir, cd, ls, cp, rm ...

[quiz1](./task_linux_cli/quiz1.png)
[quiz2](./task_linux_cli/quiz2.png)
[quiz3](./task_linux_cli/quiz3.png)
[quiz4](./task_linux_cli/quiz4.png)

Мала поняття про структуру URL , методи запитів та статус-коди, проте інформація про з'єднання та кешування була новою, раніше лише чула про це без деталей.
Здивувало, що кешування є таким механізмом, що сприяє покращенню ефективності запит-відповідь.
В роботі здається має місце використовуватися практично все, описане в статтях - від структури рядка до кешування, методи запитів + коди відповідей

## Git Collaboration

Git is both cool and difficult )) Everything is clear when you are watching a video, but on real repo a lot goes wrong
I do notes of command and hope it will help me in practice. I know I have to repeat few times doing commands to resolve different situations

My tasks:
[learngitbranching](./task_git_collaboration/learngitbranching.png)
[learngitbranching](./task_git_collaboration/learngitbranching_1.png)
[week_3](./task_git_collaboration//week_3.png)
[week_4](./task_git_collaboration//week_4.png)
[tests](./task_git_collaboration/tests1.png)
[tests](./task_git_collaboration/tests2.png)
[tests](./task_git_collaboration/tests3.png)
[tests](./task_git_collaboration/tests4.png)

I liked this [super INFO ](https://github.com/k88hudson/git-flight-rules) and [another INFO](https://ohshitgit.com/) think will help me for first time

## Intro to HTML and CSS

Having some base I`ve refreshed my knowledge in HTML and CSS, especially about box model, positioning, combining selectors. Absolutely new was information about float.
I think all this is used in work, because it is a base for building pages.

##### Some notes to remember

- h1.special - select only the h1 elements with a class of special;
- .main-list li - descendant combinator select li that are descendants of the .main-list. Nested elements can be selected by separating selectors with a space

**float** - determines how far left or how far right an element should float within its parent element. The value left floats an element to the left side of its container and the value right floats an element to the right side of its container. For the property float, **the width of the container must be specified** or the element will assume the full width of its containing element.

**clear** - specifies how an element should behave when it bumps into another element within the same containing element.The clear is usually used in combination with elements having the CSS float property. This determines on which sides floating elements are allowed to float.

Position:

- **relative** - an element is relative to its default position on the page
- **absolute** - an element’s position is relative to its closest positioned parent element. It can be pinned to any part of the web page, but the element will still move with the rest of the document when the page is scrolled
- **fixed** - an element’s position can be pinned to any part of the web page. The element will remain in view no matter what.
- **sticky** - an element can stick to a defined offset position when the user scrolls its parent container.

My tasks are here:

- [week_1](./task_html_css_intro/week_1.png)
- [week_2](./task_html_css_intro/week_2.png)
- [learn_html_css](./task_html_css_intro/learn_html_css.png)

I liked this very much ) [Can't Unsee ](https://cantunsee.space/)

## Responsive Web Design

Great article **Responsive web design basics**, it gives good overview on responsive with links to another articles for details.

I was familiar with flexbox, but refreshed it in mind.

The first to remember - we need metatag in the head `<meta name="viewport" content="width=device-width, initial-scale=1">`
`width=device-width` sets the width of the viewport to the width of the device.
`initial-scale=1` sets the initial zoom level when the user visits the page.

From the video **about flexbox** new and interesting was info about flex-basic and flex property.

**_To get space between flex-elements_** - set negative margin which is half of needed space to parent container and the same figure of padding (left and right) to elements of container.

_flex: flex-grow flex-shrink flex-basis_ - sets how a flex item will grow or shrink to fit the space available in its flex container.

To let some flex-element to grow (to strech for free space) - flex: 1 1 auto

In case both **flex-basis** (other than auto) and **width** (or **height** in case of flex-direction: column) are set for an element, **flex-basis** has priority.

Grids was really new for me, look great, I`ll try to use in next task to practice.

Games

- [flexbox_froggy](./task_responsive_web_design/flexbox_froggy.png)
- [cssgridgarden](./task_responsive_web_design/cssgridgarden.png)

## HTML-CSS-Popup

It was not difficult, but interesting). It`s interesting to practice such a kind of functionality without using JS. I practice grids, because I have never known it before. It was sucsessfull, but unusual after flexbox. I think I will use grids further.

[Demo](https://marharytaboichenko.github.io/HTML-CSS-Popup/)
[Code](https://github.com/MarharytaBoichenko/HTML-CSS-Popup)

## JS Basics

I am familiar with JS so thi material was not new for me. But it was good to repeat, especially methods of strings and arrays. Unfortunately last task was not very easy, part of it I did, but for part I needed to read more. I realize I need more practice in different tasks, it seems to me I know theory but cannot do something(.

I think everything of this unit is important and used in everyday codding, so I need more and more practise.

Also very useful is this table - game about [equility](https://eqeq.js.org/)

Tasks

- [freecodecamp](./task_js_basics/freecodecamp.png)
- [freecodecamp](./task_js_basics//freecodecamp1.png)
- [freecodecamp](./task_js_basics/freecodecamp2.png)
- [coursera](./task_js_basics/coursera.png)
