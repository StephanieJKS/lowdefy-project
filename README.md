# lowdefy-project

This project is an application for a restaurant. This restaurant is "Pizza House". Using this application, users can review the restaurant; view the restaurant's rating and read written reviews.

MongoDB is used to store the data of the reviews made. Each review consists of the reviewer's name, food rating, service rating, atmosphere rating, overall rating and a section for additional comments.

This Lowdefy application consists of four pages

## Running this project

* Create a MongoDB cluster and get a URI connection string:
  * Create a free MongoDB database cluster hosted by MongoDB Atlas.
  * Create a new database called `resaurant` with a collection called `reviews`.
    * In the Database section, click `Browse Collections` under the created cluster.
    * Click on `Create Database` and set the `Database Name` to "restaurant" and the `Collection Name` to "reviews".
    * Click on `Create` and it is good to go.
  * In the Database access section, create a database user with read access to any database.
  * In the main cluster view, click `connect`, then `Connect you application`. This will give a MongoDB URI connection string. Use the credentials you just created.
* Clone this repository.
* Create a .env file in your project folder and set your MongoDB database connector URI as a variable in the .env file: `MONGODB_URI = {{ your_mongodb_connection_uri }}`
* In the command console, navigate to your project folder and run the Lowdefy CLI: `npx lowdefy@latest dev`.

Note: 
* In the `home.yaml` file, line 68 should be changed as needed. Must be the url of the "Review Us" page.
* The "ratings" and "written reviews" pages do not handle the case for when the "reviews" collection is empty in an elegant fashion. This means that the objects are rendered without any data, i.e empty pie charts and empty containers.
