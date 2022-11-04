# 13 Object-Relational Mapping (ORM): E-Commerce Back End

## Project description

This is a backend application providing API endpoints for the front end to use to display their store. It was built using Node.js, Express, Sequalize, and express

## Mock-Up

The following animation shows the application's GET routes to return all categories, all products, and all tags being tested in Insomnia:

![In Insomnia, the user tests “GET tags,” “GET Categories,” and “GET All Products.”.](https://drive.google.com/file/d/1WEvDfIrg2GjyJdwqvb5C1eW1rz3MFlq8/view)



## Usage Tips

For more information - Please visit the following videos on how the application works and some background information on the app build.

If you want to run locally preform the following:

This application is running under mysql as a local host, you can modify the .env file with your own user/password to start the application.

If you are still intersted in running the application you would need to do the following:

run mysql terminal at project source location source db/schema.sql
npm i
npm run seed
npm start
use Insomnia (use videos and sample snapshots using Insomnia for Product model for your reference).

### Database Models

- `Category`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `category_name`

    - String.

    - Doesn't allow null values.

- `Product`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `product_name`

    - String.

    - Doesn't allow null values.

  - `price`

    - Decimal.

    - Doesn't allow null values.

    - Validates that the value is a decimal.

  - `stock`

    - Integer.

    - Doesn't allow null values.

    - Set a default value of `10`.

    - Validates that the value is numeric.

  - `category_id`

    - Integer.

    - References the `Category` model's `id`.

- `Tag`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `tag_name`

    - String.

- `ProductTag`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `product_id`

    - Integer.

    - References the `Product` model's `id`.

  - `tag_id`

    - Integer.

    - References the `Tag` model's `id`.

### Features

### links

google drive : https://drive.google.com/file/d/1WEvDfIrg2GjyJdwqvb5C1eW1rz3MFlq8/view
git hub :https://github.com/ChiemekaAnunkor/ecommerce-backend
 

API 
### contact

After creating the models and routes, run `npm run seed` to seed data to your database so that you can test your routes.

### liscences

Create the code needed in `server.js` to sync the Sequelize models to the MySQL database on server start.

## liscences

--
MIT

© 2022 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.
