# Profile Generator 
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

  #Table of Content
  - [description](#Description)
  - [installation](#Installation)
  - [usage](#Usage)
  - [credits](#Credits)
  - [license](#License)
  - [contact](#Contact)

  ## Description:
  The purpose behind this project was to create a back end for an e-commerce site. In order to be able to create, update and delete products as you wish. The user can also access the category, products and tags by using GET method to view the JSON data in each database. Now the user will be able to more easily run inventory. 

  You can see the profile generator layout below:

   ![alt text](./assets/profile%20image.png)

  ## Installation:
  In order to be create this application the following technologies were utilized:
   
    - Express
    - Mysql2
    - Sequelize

    - Dotenv was also utilized to store configuration in a seprate location from code. Detenv loads environment variables from the .env file and moves it into process. env.


  Below, I have displayed how I utilized sequelize to create a post:

   ![alt text](./assets/get%20route.png)

  Below, I have displayed how I utilized sequelize to update a post:

   ![alt text](./assets/put%20method.png)


  Below, I have displayed how I utilized sequelize to delete a category:

  ![alt text](./assets/delete%20route.png)


  ## Usage:

 This application can be used in the following way, when user adds database name, MySQL username, and MySQL password to an environment variable file to connect to Sequelize. User will need to enter schema and seed commands. After user will be able to invoke the application. The server will start and the Sequelize models are synced to the MySQL database. You can test this applications back by using API GET routes in Insomnia for categories, products, or tags. The data for each of these routes is displayed in a formatted JSON. The user will also be able to test API POST, PUT, and DELETE routes in Insomnia and be able to create, update, and delete data in the database.

  
  
  Here you can see how I have created a relationship between Category and Product database using (hasMany):
  ```
 Category.hasMany(Product, {
  foreignKey: 'category_id',
  onDelete: "CASCADE"
});

  Here you can see how I have created a relationship between Tag and Product database using (belongsToMany):
  ```
  Tag.belongsToMany(Product, {
  foreignKey: 'tag_id',
  through: {
    model: ProductTag,
    unique: false 
    },
 });

  ```

  ## Credits:
  I utilized https://gist.github.com/lukas-h/2a5d00690736b4c3a7ba to generate markdown license badges.

 
  ## License:
  MIT 

  ## Contact:
  allleizq@gmail.com