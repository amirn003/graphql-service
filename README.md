## GraphQL Service

1. Build the application by running the following command. This will build the docker application using the docker file in the current directory and tag it graphqlservice.

    docker build . -t graphqlservice

2. Run the application that you just built on port 8080

    docker run -dp 8080:4000 graphqlservice

3. To confirm that the service is running, execute the following command.

    curl localhost:8080

4. Now, with Postman query your GraphQL service, run:

    {
        cities {
            city
            state
            }
    }

    {
        cities(state:"Florida") {
            city
        }
    }