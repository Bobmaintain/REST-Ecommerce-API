# Ecommerce API

## Table of contents

* [Introduction](https://github.com/Luis-Rene-Lopez/Eccomerce-Backend-Node#introduction)
* [Run](https://github.com/Luis-Rene-Lopez/Eccomerce-Backend-Node#run)
* [Technology](https://github.com/Luis-Rene-Lopez/Eccomerce-Backend-Node#technology)
* [Database model](https://github.com/Luis-Rene-Lopez/Eccomerce-Backend-Node#database-model)
* [Endpoints](https://github.com/Luis-Rene-Lopez/Eccomerce-Backend-Node#endpoints)
* [Licence](https://github.com/Luis-Rene-Lopez/Eccomerce-Backend-Node#licence)

## Introduction

Ecommerce REST API to implement with fronted platforms. 

## Run

To run this application, you have to set your own environmental variables. For security reasons, some variables have been hidden from view and used as environmental variables with the help of dotenv package. Below are the variables that you need to set in order to run the application:

* MONGO_URI: this is the connection string of your MongoDB Atlas database.

## Technology

* Node.js
* Express
* MongoDB
* Mongoose

## Database model

All the models can be found in the models directory created using mongoose.

## Product Schema:

* name (String)

* price (Number)

* description (String)

* ammount (Number)

* imgURL (String)

## User Schema:

* email (String)

* password (String)

## Endpoints

#### `POST` /api

Create a new product

Parameters

| Name | required  | type  | Description |
| :---:| :-:| :-:| :-:|
| name | true | String | | name of the new product
| :---:| :-:| :-:| :-:| 
| price | true | Number | | | price of the new product
| :---:| :-: | :-:| :-:|
| description | true | String | description of the new product
| :---:| :-:| :-:| :-:|
| ammount | true | Number | Available ammount of the product
| :---:| :-:| :-:| :-:|
| imgURL | true | String | Image URL of the new product

#### GET

* /:productId - Get data of a speciic product 

#### PUT

* / - Update product

#### DELETE

* /:productId - Delete product

## Licence
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

* MIT License
* Copyright 2021 © Luis Lopez
