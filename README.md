
# Welcome to airline backend projects.

This is a base node js project template,which anyone can use as it has been prepared, by keeping some of the most important code principles and project management recommendations.Feel free to change anyhthing.


`src` ->Inside the src folder all the actual source code regarding the project will reside,this will not include any kind of tests.(You might want to make seperate tests folder)

Lets take a look inside the `src` folder
 
 -`config` -> In this folder anyhting and evrything regarding any configuration or setup of a library or module will be done.For example: setting up `dotenv` so that we can use the environment variables anywhere in a cleaner fashion, thisis done in the `server-config.js`.One more example to setup you logging library that cna help you to prepare meaningful logs, so configuration for this library should also be done here.

-`routes` -> In the routes folder, we register a route and the corresponding middleware adn controllers to it.

-`middlewares` -> They are just going to intercept the incoming requests where we can write our validations,authenticators etc.

-`controllers` ->They are kind of the last middlewares as post them you call ypu business layer to execute the business logic.In contrillers we just recceives the incomming requests and data and then pass it to business layer,and once business layer returns an output, we structure the API response in controllers adn send the output.

-`repositories` -> This folder contains all the logic using which we can interact the DB by writting queries, all the raw queries or ORM queries will go there.

-`services` -> contains business logic and interacts with repositories for data from databse

-`utils` -> contains helper methods, error classes etc.


### Setup the project

- Download this template from github and open it in your favourite text editor.

- Go inside the folder and execute th efollowing command :
```
   npm install
```
- In this root directory create a `.env` file and add the following env variables

  ``` 
     PORT=<Port number of your choice>

  ```
  ex:
  ```
  PORT=3000
  ```
  -go inside the src folder and execute the following command:

  ```
     npx sequelize init

```
- By executing above command you will get migration and seeders folder along with a config.json inside the config folder.

-If you are setting uo your developement environment , then write the user name of your db,password of your db and in dialect mention whatever db you are using for ex: mysql , mariadb etc

- If you are setting up test or prod environment , make sure you also replace the host with the hosted db url.


- To run the server execute 
``` 
npm run dev

```


=======
