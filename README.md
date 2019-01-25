# dynamodb-local-persist

amazon/dynamodb-local with data persistence

# How to use
## Launch by Docker

```bash
$ docker run -p 8000:8000 -v /path/to/mount:/home/dynamodblocal/db misoca/dynamodb-local-persist
```

## Launch by Docker Compose

```yml
services:
  dynamodb:
    image: misoca/dynamodb-local-persist
    ports:
      - "8000:8000"
    volumes:
      - db-data:/home/dynamodblocal/db
volumes:
  db-data:
    driver: local
```
