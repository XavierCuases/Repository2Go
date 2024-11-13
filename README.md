# Hello world whit Go
## Results
<p align="center">
   <img src="./resultados/resultado1.png" alt="Hello from Go">
</p>

In this "Hello World" program written in Go, the application starts a basic web server that listens for HTTP requests. When a user navigates to the specified URL (usually http://localhost:9000), the server sends an HTML page in response. This page includes JavaScript code that manipulates the DOM to display the "Hello World" message. The Go program handles the backend server setup and routing, while the frontend JavaScript dynamically updates the content for the user.

## :open_book: How to use
* Clone the repository

    ```
    git clone https://github.com/XavierCuases/Repository2Go.git
    ```
> [!NOTE]
To get started, clone this repository to your computer and make sure Go is installed. The project’s main file, main.go, contains the code to start the web server. Open the project in a code editor, such as Visual Studio Code, and ensure that the Go environment is properly configured.

To run the application, open a terminal in the root directory of the project and run the main.go file. This will start the server and you can access the application through a web browser at the URL http://localhost:9000. The web page will display the message "Hello World", which is manipulated through the DOM to present itself dynamically to the user.


## :rocket: How to run in docker
### Pre-requisites
* Docker - DockerDesktop installed
* DockerHub account

### link image docker hub 


### Download image

[ImagenGO](https://hub.docker.com/r/xaviercuases/exercise2go "click for visit")

The link will be for the image to be able to download it
```
docker pull xaviercuases/exercise2go
```
> [!IMPORTANT]
> Flask, by default, runs on port 5000 when using its built-in development server. This is intended for local development and testing purposes. If you need to change the port, Flask allows you to specify a different one when running the application.
### Run image
```
docker run --name <NEWCONTAINERNAME> -d -p 9000:8080 <IMAGENAME>
```
> [!TIP]
> The name of the downloaded image must match the one placed in the previous command, for this you can verify it using the **docker images** command. Additionally, you must check that there is no other container with the same name as the one placed in the command.
### View the results
Open new window browser and search localhost:9000

[View results](#results)

## :light_rail: PAAS Deploy with docker (render)
For its deployment in a PAAS we will rely on Render and its easy implementation thanks to its container management. 

![Render Service](./resultados/render4.png "Service")

This project is deployed on Render, which supports multiple programming languages:

Docker
Elixir
Go
Node.js
Python 3 (used in this project)
Ruby
Rust
This project uses Go to run a web application on Render. Simply select "Go" during deployment, connect your repository, and follow Render’s setup instructions.

![Build Container](./resultados/render2.png "Build Configuration")

> [!IMPORTANT]
> Next, This project is configured to deploy on Render with the following settings:

Build Command: go build -o main main.go  Compila el archivo main.go y crea un ejecutable llamado main.
Pre-Deploy Command: (Opcional) Para realizar tareas previas al despliegue, como migraciones (actualmente vacío).
Start Command: go run main.go Ejecuta el archivo main.go para iniciar la aplicación.
Auto-Deploy: Yes La aplicación se despliega automáticamente cuando se actualiza el código o la configuración.


![Generate Domain](./resultados/render3.png "Domain")

[Hello World](https://repository2go.onrender.com "click for visit")
