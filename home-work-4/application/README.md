## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## other

```bash
# build and push
$ docker build -t ilialikovmsk/homework-4:latest .
$ docker push ilialikovmsk/homework-4:latest
$ docker run -p 3000:8000 ilialikovmsk/homework-4:latest
# run localc mongdb   mongodb://admin:password@localhost:27017/db-name
$ docker-compose -f docker-compse-local-mongo.yaml up -d
```
