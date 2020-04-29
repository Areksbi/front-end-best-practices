# Front End - Best practices
Some best practices or choices I found in my experience.
*Always available for suggestions 😊*

## Index
#### [1. Git](#git)
#### [2. Choose technology for enterprise projects](#choose-technology-for-enterprise-projects)
##### - [2.1 Vanilla](#vanilla)
##### - [2.2 Angular](#angular)
##### - [2.3 React](#react)

## <a name="git"></a>1. Git
- Pull requests / Merge requests
- Commit messages
  - https://github.com/RomuloOliveira/commit-messages-guide/blob/master/README.md
- Branches like [gitflow](https://nvie.com/posts/a-successful-git-branching-model/)
  - ```master```: production only
  - ```develop```: where all **features** will be merged in, the ONLY branch mergable in ```master```
  - ```feature/#id-brief-description```: opened from ```develop``` and mergable in ```develop```, describe a feature task. Replace ```id``` with the id of the task, succeded by a brief description of the task
  - ```hotfix/#id-brief-description```: opened from ```master``` and mergable in ```master``` and ```develop```, describe a fix for **production**. Replace ```id``` with the id of the bug, succeded by a brief description of the fix
  - ```bugfix/#id-brief-description```: opened from ```develop``` or ```feature``` and mergable in the branch you opened from, describe a fix for a feature. Replace ```id``` with the id of the bug, succeded by a brief description of the fix
  - ```release/name-release```: opened from ```master``` and mergable in ```master``` when it's ready, daily updated with ```master```

## <a name="choose-technology-for-enterprise-projects"></a>2. Choose technology for enterprise projects
### <a name="vanilla"></a>2.1 Vanilla
- My preferred choise but need a senior Front End dev
- Create your own bundle: https://createapp.dev/
- It's not easy to create a good Vanilla architectur
### <a name="angular"></a>2.2 Angular
- With a lot of rollover on the team
- Easiest for new entries
- A lot of forms to handle
- Not the best to learn Javascript
### <a name="react"></a>2.3 React
- With a lot of rollover on the team
- Useful to learn Javascript better
- Tranding choice

## 3. HTML

## 4. CSS

## 5. Javascript

## 6. IDE

## 7. Images

## 8. Doc

## 9. Teamwork

## 10. Tool
