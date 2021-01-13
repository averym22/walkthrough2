# Installation and Setup

1. `cd express_postgres`
2. `npm install`
3. `cd docker_compose`
4. `docker-compose up --build -d`
5. Wait for the database to initialize. 30 seconds should do.
6. `cd ../ && npm start ` to start server

# Testing

1. `npm run test`
   --runs test for all template endpoints NOTE: The test suite contains the same test many times in a loop. This looped test is there because mocha does not wait for the backend to connect to the database before it runs tests. With the loop, we slow mocha down enough that the backend can connect to the database.
2. `npm run coverage`
   --shows testing coverage for all template endpoints NOTE: You will need to CTRL+C after the tests pass to see the code coverage
