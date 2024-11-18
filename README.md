# Go Bookstore Project

## Steps to Run the Project

1. **Initialize the Go Module**  
   Run the following command to initialize the project as a Go module:
   ```bash
   go mod init github.com/64anushka/go-bookstore
    ```
    
2. **Install Required Dependencies**
    Install the necessary packages:

    ```bash
    go get github.com/gorilla/mux
    go get github.com/jinzhu/gorm
    go get github.com/jinzhu/gorm/dialects/mysql
    ```

3. **Build and Run the Project**  
   - Before running the project, ensure the following:
     - **MySQL** is installed and running on your system.
     - A MySQL user named `anushka` is created with the password `your_password`.
     - A database named `simplerest` is created in MySQL and accessible to the `anushka` user.

     To set up MySQL, follow these steps:
     ```sql
     CREATE USER 'anushka'@'localhost' IDENTIFIED BY 'your_password';
     CREATE DATABASE simplerest;
     GRANT ALL PRIVILEGES ON simplerest.* TO 'anushka'@'localhost';
     FLUSH PRIVILEGES;
     ```

   - Navigate to the `cmd/main` directory:
     ```bash
     cd cmd/main
     ```
   - Build the project:
     ```bash
     go build
     ```
   - Run the project:
     ```bash
     go run main.go
     ```
   - The application should now be running. You can test the API endpoints using [Postman](https://www.postman.com/) or any other API testing tool.
