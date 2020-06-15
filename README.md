# Squarespace Website Workflow

## Dev setup:

The typical dev setup is to have the repo with two remotes:

* `github` where most developer activity takes place (the default repo)
* `square` where we push to go live

I think to get this you

1. Do the usual dance with the `clone` button from https://github.com/STL-Mutual-Aid-Developers/squarespace-src , for example, with ssh:

```
git clone git@github.com:STL-Mutual-Aid-Developers/squarespace-src.git
```

2. Rename the remote from `origin` to `github`

```
git remote rename dev github
```

3. Add the squarespace remote, which includes what's deployed to the website

```
git remote add square https://stl-mutual-aid.squarespace.com/template.git
```

### Result

I think after that we `git push/pull` from Github by default, and can deploy with `git push square master`
