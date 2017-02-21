# README

Learn how to add pagination to an API in Rails. Application is built and run using docker & docker-compose.

[Episode video link](https://youtu.be/DgfTbTB5ypQ)

[![Episode Video Link](https://i.ytimg.com/vi/DgfTbTB5ypQ/hqdefault.jpg)](https://youtu.be/DgfTbTB5ypQ)

## Tested on

* macOS - 10.12
* Docker - 1.12.6
* Docker compose - 1.9.0

## Run this application

```
git clone git clone https://github.com/devteds/e4-rails-api-pagination.git
cd e4-rails-api-pagination
# edit docker-compose.yml to set the mysql & rails ports to be mapped on host
docker-compose build
bin/d_rails db:migrate
bin/d_rails db:seed
# Use REST client or curl to browse the APIs
http://localhost:3002/posts
```
