# README

Learn how to create a Rails API-only application. Create and run with docker.

[Episode video link](https://youtu.be/pTgaCgfH6_U)

[![Episode Video Link](https://i.ytimg.com/vi/pTgaCgfH6_U/hqdefault.jpg)](https://youtu.be/pTgaCgfH6_U)

## Tested on

* macOS - 10.12
* Docker - 1.12.6
* Docker compose - 1.9.0

## Video - Instructions / commands

```
mkdir ~/projs
git clone git@github.com:ec-codecasts/docker-rails-template.git blog-api
cd blog-api
rm -rf .git
docker-compose run app rails new . --force --database=mysql --skip-bundle --api
# Edit Gemfile to uncomment to include jbuilder gem
docker-compose build
docker-compose up
# http://localhost:3001
docker-compose run --rm app rails g scaffold post title body:text
docker-compose run --rm app rake db:migrate
# GET http://localhost:3001/posts.json
# POST http://localhost:3001/posts.json with JSON body
```
