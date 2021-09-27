# gwc-demo

# Tools you can use
- Create a github account https://github.com/
- Install git https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
- Install hugo https://gohugo.io/getting-started/installing/
- Install VSCode https://code.visualstudio.com/

# Instructions on how to do this
Create a new repo in GitHub with a name you like for your site. 

Choose a directory to work from on your computer.
In a terminal window and navigate to that directory.
```
hugo new site my-site-name // (replace my-site-name with the name of your site)
cd my-site-name
git init -b main
git add .
git commit -m 'new site'
git remote add origin THE-URL-OF-THE-REPO-YOU-CREATED
git push --set-upstream origin main
```

Find a hugo theme you like and configure it. I used: https://themes.gohugo.io/base16/ 
(To include theme, don't use git clone, use 
```
git submodule add https://github.com/htdvisser/hugo-base16-theme.git base16)
```

Update config.toml
- Set your baseURL to https://MYGITID.github.io/site-name
- Set title to a descriptive title of your site
- Set theme = "base16" //Or whatever theme you used

Follow instructions here to setup an Action to publish your site:
https://gohugo.io/hosting-and-deployment/hosting-on-github/

Push code to remote
```
git add .
git commit -m "First site publish"
git push
```

Checkout the "Actions" tab in your repo to see if your build succeeded and debug any issues.

Got to "Setings" on your GitHub repo and change "pages" source go gh-pages branch and /(root), click "Save"

Navigate to the URL shown on the page to see if your site is published!
