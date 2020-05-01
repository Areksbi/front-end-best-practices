# Front End - Best practices
Some best practices I have found for Front End projects in Consulting.<br>
*Always available for advices 😊*

## Index
#### [1. Git](#git)
#### [2. Choose technology for enterprise projects](#choose-technology-for-enterprise-projects)
##### - [2.1 Vanilla](#vanilla)
##### - [2.2 Angular](#angular)
##### - [2.3 React](#react)
#### [3. HTML](#html)
#### [4. CSS](#css)
#### [5. Javascript](#javascript)
#### [6. Utility](#utility)
#### [7. Images](#images)
#### [8. Tests](#tests)
#### [9. Performance](#performance)
#### [10. Front End architectures](#front-end)

## <a name="git"></a>1. Git
- Name **branches** like [gitflow](https://nvie.com/posts/a-successful-git-branching-model/):
  - ```master```: production only
  - ```develop```: where all **features** will be merged in, the ONLY branch mergable in ```master```
  - ```feature/#id-brief-description```: opened from ```develop``` and mergable in ```develop```, describe a feature task. Replace ```id``` with the id of the task, succeded by a brief description of the task
  - ```hotfix/#id-brief-description```: opened from ```master``` and mergable in ```master``` and ```develop```, describe a fix for **production**. Replace ```id``` with the id of the bug, succeded by a brief description of the fix
  - ```bugfix/#id-brief-description```: opened from ```develop``` or ```feature``` and mergable in the branch you opened from, describe a fix for a feature. Replace ```id``` with the id of the bug, succeded by a brief description of the fix
  - ```release/name-release```: opened from ```master``` and mergable in ```master``` when it's ready, daily updated with ```master```
- [Pull requests / Merge requests](https://www.atlassian.com/git/tutorials/making-a-pull-request): use them to check the code before merges in your main branches
- [Commit messages](https://github.com/RomuloOliveira/commit-messages-guide/blob/master/README.md): understanding the importance of commit messages and how to write them well

## <a name="choose-technology-for-enterprise-projects"></a>2. Choose technology for enterprise projects
### <a name="vanilla"></a>2.1 Vanilla
- My preferred choise but need Senior Front End devs
- Create your own bundle: https://createapp.dev/
- It's not easy to create a good Vanilla architecture
### <a name="angular"></a>2.2 Angular
- Use if you have a lot of rollover on the team
- Easiest for new entries
- If you have a lot of forms to handle
- Not the best to learn Javascript
### <a name="react"></a>2.3 React
- Use if you have a lot of rollover on the team
- Useful to learn Javascript
- Tranding choice
- Better for reactive rendering for complex design

## <a name="html"></a>3. HTML
- Use **HTML5** for:
  - semantic page structure
  - accessibility (**a11y**)
  - SEO
- **HTML5** links:
  - [Official doc](https://html.spec.whatwg.org/multipage/)
  - [MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
  - [The importance of semantic HTML](https://medium.com/adalab/the-importance-of-semantic-html-78e74fb75ff0)
- Some **a11y** Chrome extensions:
  - [WAVE](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)
  - [axe](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd)
  - [ChromeVox](https://chrome.google.com/webstore/detail/chromevox-classic-extensi/kgejglhpjiefppelpmljglcjbhoiplfn)
  - [HTML5 Outliner](https://chrome.google.com/webstore/detail/html5-outliner/afoibpobokebhgfnknfndkgemglggomo)
  - [Web Developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm)
- Awesome **a11y** tutorial to UNDERSTAND how to write accessible HTML: https://www.w3.org/WAI/tutorials/
- Use **Prettier** formatter to have clean HTML

## <a name="css"></a>4. CSS
- Use preprocessor (suggested [**Sass**](https://sass-lang.com/)): allows you make the development easiest
- Use [BEM](http://getbem.com/): keep your classes with a good structure
- Avoid Bootstrap, use only if want fast-projects
- Evaluate Bootstrap alternatives:
  - Bulma
  - Materialize
  - Foundation
  - Semantic UI
- Learn [pseudo-selectors](https://hackernoon.com/understanding-pseudo-class-selectors-mg443t89): they are very useful to handle situations like "first element" or "each element to the odd position"
- Use "semantic" class names (no ".is-red" or similar classes, create MIXINS with Sass instead)
- Use **Prettier** formatter to have clean CSS/Sass


## <a name="javascript"></a>5. Javascript
- [jsDoc](https://jsdoc.app/): keep your Javascript documented
- Use **eslint**: check your code with specific rules (suggest [AirBnb](https://www.npmjs.com/package/eslint-config-airbnb)'s linter)
- Prefer **Typescript**<a name="typescript"></a>: if you want a well-structured code
- Use **ES6** and above: the last Javascript versions keep your code clean and more efficent
- Be updated with new Javascript versions and use them with **Babel**
- Place the scripts at the end of the body to improve performance
- Avoid globals variables
- Use [**declarative**](https://codeburst.io/imperative-vs-declarative-javascript-8b5e45a602dd) Javascript: it keeps your code  clean and reduces the possibility of introducing bugs
- Avoid heavy nestings: keep it simple and you will easily find bugs (you will ALWAYS have bugs 🙂)
- DOM access is the heaviest (and slowest) part in JS
- Make it **understandable**: call things by their name — easy, short and readable variable and function names, it helps  everyone to understand what a variable or function is used for
- Use === instead of ==
- ```eval``` is evil
- Avoid setTimeout and setInterval even more: they can introduce bugs difficult to find


## <a name="utility"></a>6. Utility
- Suggested **IDE** (Integrated development environment):
  - **WebStorm** (pay): a great workplace, the best I used for FE development
  - **Visual Studio Code** (free): the best I tried for free, with a lot of extensions
  - **Atom** (free): valid VS Code alternative
  - **Sublime** (free): valid VS Code alternative
- Use **regions** to split your code and make it collapsable with the most of IDEs (here an [example](http://vswebessentials.com/features/javascript#regions) with Javascript, but can be used everywhere)
- Use **TODO** or **FIXME** when you are going to commit files you have to rework ([example](https://help.semmle.com/wiki/pages/viewpage.action?pageId=29393692) in Java)
- Add [**change log**](https://desmart.com/blog/how-to-generate-your-project-s-changelog-from-commit-messages): it allows you to document your releases, "Clients love it = you'll love it"
- Add **precommit** and/or **prepush** to check or format your code (suggested **husky** with **lint-staged**)
- Add **.editorconfig** ([link](https://editorconfig.org/)): keep the same formatting between different people's IDEs
- Add docs
- Use **English** language in your code, please

## <a name="images"></a>7. Images
- Icons: prefer **SVG** if you have [HTTP2](#http2) or iconfonts if without HTTP2. Avoid sprites or plain images.
- Load best image based on screen width ([responsive images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images))
- Optimize images (https://kinsta.com/blog/optimize-images-for-web/ or tool online)

## <a name="tests"></a>8. Tests
- Use [**Cypress**](https://www.cypress.io/) for e2e (end to end) tests, very fast to write and can reduce problems in the future; they run on Chrome
- I think **Unit Tests** are a bit useless in FE development since they don't reproduce the browser situation

## <a name="performance"></a>9. Performance
- Optimize resources and loadings (https://www.smashingmagazine.com/2019/04/optimization-performance-resource-hints/)
- Use [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/), it has also a lot of suggestions for every negative point the site has
- Use [WebPageTest](https://www.webpagetest.org/): test your pages speed with nice tools
- Use <a name="http2"></a>**HTTP2** (or HTTP3 when it will be fully available): its the protocol used on your server to send resources to your client, with HTTP2 you can load your resources asynchronously
- Sometimes **UX** has a great impact on the "visual performance"
- Use **lazy loading**: you can load only-when-in-viewport images or features

## <a name="front-end"></a>10. Front End architectures
- My favorite is the biologic-system:
  - **atoms**: base components like inputs, titles, etc
  - **molecules**: more atoms togheter, like a form
  - **organism**: more molecules togheter, the page of the site
- Create modules for every feature and load them with lazy loading only when needed
- Use [**Typescript**](#typescript) with its structures (Interfaces and so on)
- Use verified [**npm packages**](https://www.npmjs.com/) for some annoying feature to develop (ex: accordions, sliders, etc.)
