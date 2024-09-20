# EasyNotes Application

# this is a guide, is the step for step running application

1. create data base in this case is mongo database, and you need to use a new image instance of the mongo image in Docker

2. using env variables for database connection
    1. in the file `database.config.js` change the `URI` of the database a example is:
        ```js
        const dotenv = require("dotenv")
        dotenv.config()

        const host = process.enb.DB_HOST || "localhost"
        // in next line define all env variables for the database URI
        // a example URI is => mongodb://<user>:<password>@<host>:<port>/<db name>

        module.exports = {
            url: 'mongodb://localhost:27017/easy-notes'
        }
        ```

3. send your env variables via .env file or directly for docker container
