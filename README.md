This is a base express-mongo project template which anyone can use as it has been prepared by keeping some of the most important code principles and project management recommendations. Feel free to change anything.

`src` -> inside the src folder all the actual source code regarding the project will reside this will not include any kind of tests (you might want to make a separate tests folder)

lets take a look inside the src folder

- `config` -> In this folder, anything and everyhting  regarding any configurations or setup of a library or module will be done. For example, setting up dotenv so that we can use the environment variables in a cleaner fashion, which is done in the `server.config.js` file. All the database related configurations are also done here.

- `routes` -> In the routes folder, we register a route and the corresponding middleware and controllers to it. In the routes foulder there are folders named v1, v2, .... for api versioning.

- `middlewares` -> they aare just going to intercept hte incoming requests where we can write our validators authenticators etc.

- `controllers` -> they are a kind of the last middlewares as post them you callyour business layer to execute the business logic. In controllers we just recieve the incoming requests and data and then pass it to the business layer. And once busineess layer returns an output, we structure the API response in controllers and send the output.

- `repository` -> this folder contains all the logic using which we interact with the database by eriting queries, all the raw queries or ORM queries will come under here.

- `services` -> It contains all the business loguc and interacts with repository for data from the database.

- `utils` -> It contains helper methods, error classes etc.

- `seeders` -> It is used for testing purposes. It puts a seed data (starting data) for your tables. Also it can be used for assigning roles in test, developemnt, prodcution environments.

- `migrations` -> These files are used for version control of your database. These are simple langauge scripts where we write programmatically that how to maintain versions of your database depending upon the unique ids of your database.

### Setup the project

- Download this template from github and open it in your favorite text editor .

- In the root directory create a `.env` file and add the following env variables
    ```
        PORT=<port number of your choice>
    ```
    ex:
    ```
        PORT=3000
    ```
    