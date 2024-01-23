# test quarto website

1. `git init` a `quarto website` project folder and sync it with `github remote repo`

2. add the following in `_quarto.yml` in the quarto website project folder
```yaml
project:
  type: website
  output-dir: docs
```

3. add an empty file `.nojekyll` in `root dir` of the project
```shell
touch .nojekyll
```

4. preview the quarto website
```shell
quarto preview
# or, use keybidning <space-q-p> in nvim to activate quarto preview
```

5. stop quarto preview, and sync the quarto website repo so that the docs folder on github is updated

6. check the `Deployments` section of the git repo 

Ref: [quarto guide > publishing > github pages](https://quarto.org/docs/publishing/github-pages.html#publish-command)
