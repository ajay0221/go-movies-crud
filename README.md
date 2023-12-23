# Go Movies CRUD

This is a simple CRUD (Create, Read, Update, Delete) application written in Go, using the Gorilla Mux router for handling HTTP requests.

## Project Structure

The project consists of a single Go file, `main.go`, which contains all the code for the application.

## Code Explanation

1. The code starts by importing necessary packages, including the Gorilla Mux router and the standard library packages for handling HTTP requests and JSON.

2. Two struct types, `Movie` and `Director`, are defined. These structs are used to model the data in the application.

3. A slice of `Movie` structs, `movies`, is declared to store the movie data.

4. Several functions are defined to handle HTTP requests:

    - `getMovies`: This function handles GET requests to the "/movies" endpoint. It returns a JSON representation of all movies in the `movies` slice.

    - `getMovie`: This function handles GET requests to the "/movies/{id}" endpoint. It returns a JSON representation of the movie with the specified ID.

    - `createMovie`: This function handles POST requests to the "/movies" endpoint. It creates a new movie from the JSON in the request body and adds it to the `movies` slice.

    - `updateMovie`: This function handles PUT requests to the "/movies/{id}" endpoint. It updates the movie with the specified ID with the data in the request body.

    - `deleteMovie`: This function handles DELETE requests to the "/movies/{id}" endpoint. It removes the movie with the specified ID from the `movies` slice.

5. In the `main` function, the Gorilla Mux router is initialized and several routes are set up to handle the different endpoints and HTTP methods. Some initial movie data is also added to the `movies` slice.

6. Finally, the HTTP server is started on port 8000, with the router handling incoming requests.

## Running the Application

To run the application, you need to have Go installed on your machine. Once you have Go installed, you can run the application using the following command:

```bash
go run main.go
```

This will start the server on port 8000. You can then interact with the API using a tool like curl or Postman.

# Dependencies

* Gorilla Mux: A powerful HTTP router and URL matcher for building Go web servers.

# License
This project is open source and available under the MIT License.