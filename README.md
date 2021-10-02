# Ecommerce REST API

![alt text](https://news.america-digital.com/wp-content/uploads/2021/04/El-boom-del-eCommerce-tendencias-para-el-2021.jpg)

## Table of contents

* [Introduction](#introduction)
* [Technology](#technology)
* [Database model](#database-model)
* [Installation](#installation)
* [Run](#run)
* [Endpoints](#endpoints)
* [Licence](#licence)

## Introduction

Ecommerce REST API to implement with any fronted platform. 

## Technology

* Node.js
* Express
* MongoDB
* Mongoose

## Database model

All the models can be found in the models directory created using mongoose.

### Product Schema:

* name (String)

* price (Number)

* description (String)

* ammount (Number)

* imgURL (String)

### User Schema:

* name (String) 

* email (String)

* password (String)


## Installation

1. Clone this repository  `git clone https://github.com/Luis-Rene-Lopez/Ecommerce-REST-API`

2. Go to the project `cd Ecommerce-REST-API`

3. Install the project dependencies `npm install`

## Run

To run this application, you have to set your own environmental variables. For security reasons, some variables have been hidden from view and used as environmental variables with the help of dotenv package. Below are the variables that you need to set in order to run the application:

* MONGO_URI=  This is the connection string of your MongoDB Atlas database.

* PORT=  This is the port number for running the Node.js server. 

## Endpoints

### User registration

![POST](https://img.shields.io/badge/METHOD-POST-blue) **`/api/auth/register`**

Body parameters:

| Name | Required  | Type  | Description |
| :---:| :-:| :-:| :-:|
| name | true | String | User name |
| email | true  | String | User email address |
| password | true | String | User password |

### User login

![POST](https://img.shields.io/badge/METHOD-POST-blue) **`/api/auth/login`**

Body parameters:

| Name | Required  | Type  | Description |
| :---:| :-:| :-:| :-:|
| email | true  | String | User email address |
| password | true | String | User password |


### Create new product

![POST](https://img.shields.io/badge/METHOD-POST-blue) **`/api`**

* Requires token-based authentication

Body parameters:

| Name | Required  | Type  | Description |
| :---:| :-:| :-:| :-:|
| name | true | String | Name of the new product
| price | true | Number | Price of the new product
| description | true | String | Description of the new product
| ammount | true | Number | Available ammount of the product
| imgURL | true | String | Image URL of the new product

### Get details of a specic product

![GET](https://img.shields.io/badge/METHOD-GET-brightgreen) **`/api/:productId`**  

* Requires token-based authentication

### Update product

![PUT](https://img.shields.io/badge/METHOD-PUT-yellow) **`/api`**

* Requires token-based authentication.

Body parameters:

| Name | Required  | Type  | Description |
| :---:| :-:| :-:| :-:|
| productId | true | String | Product ID |
| name | true | String | Product new name
| price | true | Number | Product new price
| description | true | String | Product new description
| ammount | true | Number | Product new available ammount
| imgURL | true | String | Product new image URL

### Delete product

![DELETE](https://img.shields.io/badge/METHOD-DELETE-red) **`/api/:productId`**

* Requires token-based authentication

## Licence
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

* MIT License
* Copyright 2021 © Luis Lopez
