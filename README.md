# postman-api
Регистрируемся (Registration):
POST https://blog-platform.kata.academy/api/users:
//request
{
  "user": {
    "username": "stringSTRING",
    "email": "string@yandex.ru",
    "password": "string"
  }
}
//response
{
    "user": {
        "username": "stringstring",
        "email": "string@yandex.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3NjIwODEzY2UxOGQwMWIwMDJiNjVlMSIsInVzZXJuYW1lIjoic3RyaW5nc3RyaW5nIiwiZXhwIjoxNzM5NjYxODQzLCJpYXQiOjE3MzQ0Nzc4NDN9.QSMO0aAUPV93tgdsyuYkm8dr6UOCjtxQGLFMWViIv3M"
    }
}


Логинимся (Authentication):
POST https://blog-platform.kata.academy/api/users/login:
//request
{
  "user": {
    "email": "string@yandex.ru",
    "password": "string"
  }
}
//response
{
    "user": {
        "username": "stringstring",
        "email": "string@yandex.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3NjIwODEzY2UxOGQwMWIwMDJiNjVlMSIsInVzZXJuYW1lIjoic3RyaW5nc3RyaW5nIiwiZXhwIjoxNzM5NjYyMTkxLCJpYXQiOjE3MzQ0NzgxOTF9.VizS_uqcGdnhj62P7E4u-5QxdPkFnmalZ5n1Q5DSHts"
    }
}

Используя заголовок авторизации получить данные текущего пользователя:
GET https://blog-platform.kata.academy/api/user
//request
Authorization Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3NjIwODEzY2UxOGQwMWIwMDJiNjVlMSIsInVzZXJuYW1lIjoic3RyaW5nc3RyaW5nIiwiZXhwIjoxNzM5NjYyMTkxLCJpYXQiOjE3MzQ0NzgxOTF9.VizS_uqcGdnhj62P7E4u-5QxdPkFnmalZ5n1Q5DSHts
//response
{
    "user": {
        "username": "stringstring",
        "email": "string@yandex.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3NjIwODEzY2UxOGQwMWIwMDJiNjVlMSIsInVzZXJuYW1lIjoic3RyaW5nc3RyaW5nIiwiZXhwIjoxNzM5NjYyNjIyLCJpYXQiOjE3MzQ0Nzg2MjJ9.k25kzIsgf8YO0poELaoXa1eSiMNn26ov7ryKMAOh3NE"
    }
}
