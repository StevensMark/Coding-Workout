Practice these coding skills daily until they become part of working memory.

# Contents
* [Build new project using GitHub](#github)
* [Steps for using Git in a software dev group project](#git)
* [Resolve common errors](#errors)
* [Angular](#angular)
* [Flask](*flask)

*****

# Build new project using GitHub <a name="github"></a>

1. Create new repository in GitHub
2. Clone repository to local machine
3. Build project; i.e. Gatsby, Angular, etc
4. Push changes to GitHub

### Create new repository in GitHub

[![chrome-t-IIsw-Rz-Ms-L.png](https://i.postimg.cc/VsxXXGCH/chrome-t-IIsw-Rz-Ms-L.png)](https://postimg.cc/mhScsSVQ)


### Capture the repository url

[![chrome-tibt2-Ns-Zuh.png](https://i.postimg.cc/qBh8hVz3/chrome-tibt2-Ns-Zuh.png)](https://postimg.cc/HjmJRN0Y)


### Clone repository to local machine
On local machine, point to the directory where you want the GitHub repo cloned. In this example, it will be inserted in the Dev folder.

```markdown
C:\Users\StevensMark\Dev> git clone git@github.com:StevensMark/company_website.git
```

### Push changes to GitHub
Point to repo directory

Add all changes to git
```markdown
C:\Users\StevensMark\Dev> git add .
```

Commit changes to git
```markdown
C:\Users\StevensMark\Dev> git commit -m 'first commit'
```

Push changes to git
```markdown
C:\Users\StevensMark\Dev> git push
```


# Steps for using Git in a software dev group project <a name="git"></a>


### Clone repository to local machine

1. Create project folder
2. Point to project folder in the command line
3. Clone the repository using the SSH url

```markdown
git clone [ SSH url ]
```

### Create new branch

```markdown
git checkout -b [branch name]
```

### Open VS Code

```markdown
code .
```

Build project and/or edit code

### Stage the new code

```markdown
git add .
```

### Commit the new code
Include a short, clear message describing the new code or code revisions

```markdown
git commit -m "[message]"
```
Best practice when commiting multiple code changes is to combine those commits into
a single commit, before pushing to the repository. For example, if you made 4 commits,
then...

```markdown
git reset --soft HEAD~4
git status
git commit -m "styling ideas"
git log master.. --oneline
git push --set-upstream <name-of-branch>
git push -f
```

### Push the branch to the repository
 
```markdown
git push --set-upstream origin [branch name]
```

### Merge from MAIN to BRANCH
When changes were made to MAIN that you want to import into your BRANCH:
1. From your BRANCH in the command prompt
2. Assuming your MAIN has the name "main" 

``` markdown
git merge main 
```

<br>

# Resolve Common Errors <a name="errors"></a>

*****

## npm ERR! code ERESOLVE
ERESOLVE unable to resolve dependency tree


```markdown
npm config set legacy-peer-deps true
```
<a href="https://www.youtube.com/watch?v=vn97BdYx2K8" target="_blank">Resource link</a>

## EADDRINUSE: address already in use :::3000
Need to identify and kill processes running on port 3000

```markdown
netstat -ano | findstr :3000
```
As an example, if it determines that a process is running on port 3023, then...
```markdown
taskkill /F /PID 3024
```

<!--- Comments
Create a new repository on the command line

```markdown
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:[GitHub account]/[Repo name].git
git push -u origin main
```

…or push an existing repository from the command line

```markdown
git remote add origin git@github.com:[GitHub account]/[Repo name].git
git branch -M main
git push -u origin main
```
-->

<!--- Comments

```markdown
# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

-->

# Angular <a name="angular"></a>
*****

### Install Angular to your system
```markdown
npm install -g @angular/cli
```

### Cmd to check Angular version
```markdown
ng version
```

### Creating new Angular project
```markdown
ng new "name-of-project"
```

### Cloning an Angular repo
Remember to install packages!

```markdown
npm install
```
### ERROR: Property has no initializer and is not definitely assigned in the constructor

```markdown
@Input('title') title: string;                 Typescript can throw error

@Input('title') title: string | undefined;     Solution
```
<a href="https://monsterlessons-academy.com/posts/angular-property-has-no-initializer-and-is-not-definitely-assigned-in-the-constructor" target="_blank">Resource link</a>

# Flask <a name="flask"></a>
*****

### Virtual environment
Create (use the Command Prompt, not Powershell)
```markdown
python -m venv venv
```
Activate
```markdown
.\venv\Scripts\activate
```
Deactivate
```markdown
deactivate
```

# Run Angular+Flask+PostgreSQL App Locally
PostgreSQL
  1. Start the server

Flask
  1. Open API (Flask) in VS Code
  2. Start the Debugger
  3. Open another command prompt with virtual environment activated
  4. Enter the following commands:
```markdown
set FLASK_APP=src/run.py
flask db upgrade
```
       
Angular
  1. Open CLIENT in VS Code
  2. Enter the following command:
```markdown
ng serve
```


