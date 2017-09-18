Simple JSON server for "Movies" project 

To start using it, you have to clone this repo and do:
 
```npm install -g json-server```

inside server folder you can run it with

```$ json-server --watch db.json```

it will start on localhost:3000

it stores your "movies" data base in db.json.

it implements REST API:

`` GET http://localhost:3000/movies/1``
to fetch movie by id

`` GET http://localhost:3000/movies``
to fetch all movies

``PUT http://localhost:3000/movies/1``
to update particular movie

``DELETE http://localhost:3000/movies/1``
to delete particular movie

``POST http://localhost:3000/movies/1``
to create particular movie


for PUT and POST methods, you should pass body with the request, and add headers:
```"Content-Type": "application/json"```

body example:

```$xslt
 {
        "id": 1,
        "title": "Blah Blah",
        "posterUrl": "https://images-na.ssl-images-amazon.com/images/M/MV5BZTRmNjQ1ZDYtNDgzMy00OGE0LWE4N2YtNTkzNWQ5ZDhlNGJmL2ltYWdlL2ltYWdlXkEyXkFqcGdeQXVyNjU0OTQ0OTY@._V1_SY500_CR0,0,352,500_AL_.jpg",
        "stars": 4,
        "likes": 15,
        "actors": [
            "John Dou",
            "Al Pacino",
            "James Caan"
        ],
        "director": "Francis Ford Coppola",
        "description": "Cool movie"
    }
```



