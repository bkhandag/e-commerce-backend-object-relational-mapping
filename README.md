# e-commerce-backend-object-relational-mapping

![License](https://img.shields.io/badge/license-MIT_License-red.svg)

## Description:

Internet retail, also known as **e-commerce**, is the largest sector of the electronics industry, generating an estimated $29 trillion in 2019. E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes. This application builds out the fundamental architecture of this type of platform.

## Table of Contents:

- [Description](#description)

- [User Story](#user-story)

- [Acceptance Criteria](#acceptance-criteria)

- [Installation Instructions](#installation-instructions)

- [Link to Application of Github](#link-to-application-on-github)

- [Link to Walkthrough Video](#link-to-walkthrough-video)

- [Database Model](#database-model)

- [Questions](#questions)

## User Story

```md
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```

## Acceptance Criteria

```md
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete data in my database
```

## Installation Instructions:

- Used the [MySQL2 package](https://www.npmjs.com/package/mysql2) to connect to MySQL database and perform queries
- Used the [Sequelize](https://www.npmjs.com/package/sequelize) packages to connect your Express.js API to a MySQL database
- Used the [dotenv](https://www.npmjs.com/package/dotenv) package to use environment variables to store sensitive data.

## Link to Application on Github:

https://github.com/bkhandag/e-commerce-backend-object-relational-mapping

## Link to Walkthrough Video:

## Database Model:

Your database should contain the following four models, including the requirements listed for each model:

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

## Questions:

For additional questions, reach out to me:

Github: https://github.com/bkhandag

Email: khandagale.b.g@gmail.com
