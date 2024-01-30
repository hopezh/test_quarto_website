# test publishing quarto website on github pages


1. create a `quarto` website project
```{shell}
quarto create project website myQuartoWebsite
```


2. `git init` the quarto website project folder, sync it with the `github remote repo`
```shell
cd myQuartoWebsite
echo "# My Quarto Website" >> README.md

git init
git add .
git commit -m "init commit"
git branch -M main
git remote add origin git@github.com:hopezh/myQuartoWebsite.git
git push -u origin main
```


3. add the following in `_quarto.yml` in the quarto website project folder
```yaml
project:
  type: website
  output-dir: docs
```


4. add an empty file `.nojekyll` in `root dir` of the project
```shell
touch .nojekyll
```


5. preview the quarto website
```shell
quarto preview
# or, use keybidning <space-q-p> in nvim to activate quarto preview
```


6. stop quarto preview


7. sync the quarto website repo so that the docs folder on github is updated


8. go to `git repo` -> `settings` -> `code and automation` -> `pages` section


9. in settings for `GitHub Pages`, select `main` and `/docs` for `Branch`, and `Save` 


10. check the `Deployments` section of the git repo after a while. 


Ref: [quarto guide > publishing > github pages](https://quarto.org/docs/publishing/github-pages.html#publish-command)
