# Blog site
Blog site built with [Hugo](https://gohugo.io)

## Build & deploy
Using an alias in `~/.bashrc` or `~/.zshrc`
```
function deploy-blog() {
    cd ~/Projects/blog
    hugo
    rsync -avzog --delete --chown www-data:www-data public/ vps:/var/www/blog.rasciutto.nl/public/
    cd -
}
```
