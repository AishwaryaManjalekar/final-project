# Final-project


The Onlineshop is a virtual store on the Internet where customers can browse the catalog and select products of interest. The selected items may be collected in a shopping cart. At checkout time, the items in the shopping cart will be presented as an order. At that time, more information will be needed to complete the transaction.


![](http://imgur.com/t3teAxi.png)
### :handbag: A simple RESTful API for Purchases and Products

## Features

<b>Products Features</b>

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Add a Product | &#10004; | Ability of Add a Product on the System |
| List Products | &#10004; | Ability of List Products |
| Edit a Product | &#10004; | Ability of Edit a Product |
| Delete a Product | &#10004; | Ability of Delete a Product |
| Customer | &#10004; | Ability of Check if exists |
| Customer address | &#10004; | Ability to check if already exist |

<b>Purchase Features</b>

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Create a Cart | &#10004; | Ability of Create a new Cart |
| See Cart | &#10004; | Ability to see the Cart and it items |
| Remove a Cart | &#10004; | Ability of Remove a Cart |
| Add Item | &#10004; | Ability of add a new Item on the Cart |
| Remove a Item | &#10004; | Ability of Remove a Item from the Cart |
| Checkout | &#10004; | Ability to Checkout |

# eCommerce

**eCommerce** it's an open source software made to create an easy and simple "Shopping" website.


## Frontend:

1.*Bootstrap*.

2.*HTML*.

3.*CSS*.


## Documentation

**eCommerce** has a full API documentation made with [Swagger](https://swagger.io), you can check it by accessing [this](http://santoro.pw/eCommerce) link.


## Installation

* **eCommerce** it's splitted into two standalone RESTful API's, so you can run it on whatever port you want. Installing 
* **eCommerce** it's easy, the tutorial above will explain to you.
* **eCommerce** uses Groovy `2.4` and Grails `3.2.11`.

You can run **eCommerce** in different ways. You can go to the [Releases Page](releases/) and download the source code of the latest release, or a bundled .war or a standalone java application (.jar).

**It's recommend see the notes on [this](#notes) section.**

### Development

You can attach the .war in WebServers like **Tomcat** using the Management Interface.

If you want run the standalone `.jar` just download it, and open your CMD/Terminal and write:

**If you want RUN the Products API**

`java -jar ecommerce-products-api-XXX.jar` **OR** `./products-api/grailsw run-app`

**If you want RUN the Purchases API**

`java -jar ecommerce-purchase-api-XXX.jar` **OR** `./purchase-api/grailsw run-app`

You also can build from the sources by running the **Grails Console**, just went to one of the API's folder `purchase-api` or `products-api` and write on your CMD/Terminal the following:

`grailsw assemble`

If you want to run it in development scenario, you can also do it by **building** the sources. You have two manner to do it. You can Gradle or directly Grails. Both `products-api` and `purchase-api` comes with Groovy, Grails and Gradle standalone packages. So you can run it without the need of installing they.

**Option #1 - Run by Gradle**

`gradlew bootRun`

**Option #2 - Run by Grailsw**

`grailsw run-app`

### Production

Production Environments are focused in being ready. That means, you just need execute the Jar File.

In the Production Environment all eCommerce API's are configured to work with **MySQL** in two databases; **productsAPI** and **purchaseAPI** and to work with a default **username and password** combination:

**Note.:** Remember importing each SQL files, if using MySQL for Production. You can find them inside `products-api/src/main/sql/` and `purchase-api/src/main/sql/`

* **Username:** commerce
* **Password:** commerceapi
* **Database:** productsapi & purchaseapi
* **Port:** 3306

You can change those credentials in the `application.yaml` file. In production environments **you need import the database schema** before running the software. Both `products-api` and `purchase-api` DDL files are available on [this](sql/) folder.

### Notes

**Note.:** By default `products-api` runs on port 8080 and `purchase-api` on port 8090.

**Note.:** In all Development and Test Scenarios, eCommerce uses **H2** in-memory Database.

**Note.:** You can change your database credentials both for development/test and production scenarios in the `app-config.yml` available on each API sources root. Those configuration files can be used also externally, after building the `.jar`

**Note.:** You also can clean the sources and rebuild the sources by running `grailsw clean`

## Running Test Cases

You can easily run the **Test Cases** using the standalone Grails package built-in with both the API's. Just went to the home folder of one of them (`products-api` or `purchase-api`). And write on your CMD/Terminal:

`grailsw test-app`

## Credits

This development/educational scenario was coded and created by [Claudio Santoro](http://santoro.pw) unde the [GNU GPL v3](LICENSE) License. The objective of this repository it's as practical test of RESTful API's with Java + Groovy.
