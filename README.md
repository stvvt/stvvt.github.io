# My Personal Blog

## How to Blog (notes to myself)

0. (prerequisites) docker and docker-compose installed.
1. Clone this repo
1. Run to install hexo dependencies
    ```
    $ docker-compose run --rm blog npm i
    ```
1. Run local server
    ```
    $ docker-compose up -d
    ```

    Goto http://localhost:4000 and make sure everything is OK.

## Common Tasks

### Create New Post
```
$ docker-compose run --rm blog npm new [post|draft] <title>
```
then open `source/(_posts|_drafts)/<title>.md` in a text editor.

### Deploy
```
$ git push
```
That is, really! Travis CI will do the rest. Once the Travis CI job passes (several minutes), the new post(s) and/or updates will be visible at https://stvvt.github.io