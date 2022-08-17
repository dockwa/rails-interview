# The Wanderlust Group Code Exercise

## Instructions
Welcome to the code exercise for the Wanderlust Group! For this exercise you will be building an API for a fictional company.
The goal of this exercise is to allow you to demonstrate your ability to diagnose a set of problems and implement a good solution.
Feel free to bring in additional tools or libraries as you see fit, such as a testing library, however we would like to see a majority
of the implementation logic written and designed by you. Our goal is to get as reasonable of an understanding as possible of the following:

- how you break down a problem
- your ability to understand requirements
- how you implement and design your code
- your understanding of how a system might scale

The first step is to use this template to create a new repository on Github. This will become the repository you will share with us as
your submission. The repository contains a new [Rails API application](https://guides.rubyonrails.org/api_app.html). There
is also no included test framework, so if you choose to write tests you will need to add whichever framework you are comfortable with
as well as instructions on how to run your tests.

When we run your application we will do so in Docker using the `Dockerfile` present in this repository. If you choose to 
introduce additional dependencies (such as a database other than `sqlite`), please also include modifications to either
the `Dockerfile` or the `docker-compose.yml` file so we will be able to run the application via `docker compose up`. This is
_not a requirement_ nor is it expected in any way, however if you are comfortable making these changes please feel free to do so.
If you do choose to make changes, please document them in this README.

Below you are given a list of business requirements. Within a reasonable timeframe (spend no more than a few hours!) we 
would like you to implement the requirements as you see fit. In addition to the requirements listed, please leave time 
to fill out the [requirements questions](#requirements-questions) and address any [future concerns](#future-concerns) you 
may think of. You are also encouraged to add sections of your own to the README, such as instructions on how to use the system or how to run your tests.

## Requirements

Your task is to design an API for a fictional company, Outdoorsy. The API will primarily be used to take in customer
data as well as retrieve customer data. In addition to the requirements listed below, the following system-wide requirements 
exist:

1. Data should persist between application restarts
2. The media type for APIs should be JSON
3. The system should support running multiple instances of the API

| Requirements                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| As an API client, I want to be able to add a customer to the system via a `POST` request to `/customers`. Customers are defined by the following required fields:<br><br>1. First Name <br>2. Last Name <br>3. Email Address <br>4. Vehicle Type - one of [`campervan`, `motorboat`, `bicycle`, `sailboat`] <br>5. Vehicle Name <br>6. Vehicle length in feet - must be greater than 0                                                                                                                                                    |
| As an API client, I want to be able to view the data for an individual customer via a `GET` request to `/customers/{customerId}`                                                                                                                                                                                                                                                                                                                                                                                                          |
| As an API client, I want to be able to view a list of customers in the system via a `GET` request to `/customers`. By default the list should be sorted by the date the customer was uploaded.                                                                                                                                                                                                                                                                                                                                            |
| As an API client, I want to be able to sort the list of customers in the system by either vehicle type, customer first name, or customer last name. If a sort parameter is not provided, the sort should fall back to the default.                                                                                                                                                                                                                                                                                                        |
| As an API client, I want to be able to bulk upload a CSV file with a list of customers via a `POST` request to `/customers/bulk`. Because the CSV is coming from external legacy sources, the following requirements exist:<br><br>1. The file will have no headers<br>2. The order of the data in each row will be as follows: `first name`, `last name`, `email address`, `vehicle type`, `vehicle name`, `vehicle length`<br> 3. Vehicle lengths are strings which could be in the following formats: `32'`, `32 feet`, `32 ft`, `32’` |
| As an API client, I want to be able to delete a customer via a `DELETE` request to `/customers/{customerId}`                                                                                                                                                                                                                                                                                                                                                                                                                              |


## Requirements Questions

Did you think of any questions around the requirements you were given from the business? What were those?

## Future Concerns

Please document any future concerns you may have for this API. What would you change, if anything, if the API traffic were to increase?
Were there requirements you did not get to within the timeframe? Feel free to discuss those here as well.
