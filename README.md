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

Below you are given a list of requirements. Within a reasonable timeframe, (2-3 hours) we would like you to implement the requirements as you see fit.
In addition to the requirements listed, please leave time to fill out the [requirements questions](#requirements-questions) 
and address any [future concerns](#future-concerns) you may think of. You are also encouraged to add sections of your own to
the README, such as instructions on how to run tests.

## Requirements

Your task is to design an API for a fictional company, Outdoorsy. The API will primarily be used to take in customer
data as well as retrieve customer data. In addition to the requirements listed below, the following system-wide requirements 
exist:

1. Data should persist between application restarts
2. The media type for APIs should be JSON
3. The system should support running multiple instances of the API

| Requirements                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| As an API client, I want to be able to add a customer to the system. Customers are defined by the following required fields:<br><br>1. First Name <br>2. Last Name <br>3. Email Address <br>4. Vehicle Type - one of [`campervan`, `motorboat`, `bicycle`, `sailboat`] <br>5. Vehicle Name <br>6. Vehicle length in feet - must be greater than 0                                                                                                                                               |
| As an API client, I want to be able to view the data for an individual customer                                                                                                                                                                                                                                                                                                                                                                                                                 |
| As an API client, I want to be able to view a list of customers in the system. By default the list should be sorted by the date the customer was uploaded.                                                                                                                                                                                                                                                                                                                                      |
| As an API client, I want to be able to sort the list of customers in the system by either vehicle type, customer first name, or customer last name. If a sort parameter is not provided, the sort should fall back to the default.                                                                                                                                                                                                                                                              |
| As an API client, I want to be able to bulk upload a CSV file with a list of customers. Because the CSV is coming from external legacy sources, the following requirements exist:<br><br>1. The file will have no headers<br>2. The order of the data in each row will be as follows: `first name`, `last name`, `email address`, `vehicle type`, `vehicle name`, `vehicle length`<br> 3. Vehicle lengths are strings which could be in the following formats: `32'`, `32 feet`, `32 ft`, `32’` |
| As an API client, I want to be able to delete a customer                                                                                                                                                                                                                                                                                                                                                                                                                                        |


## Requirements Questions

Did you think of any questions around the requirements you were given from the business? What were those?

## Future Concerns

Please document any future concerns you may have for this API. What would you change, if anything, if the API traffic were to increase?
Were there requirements you did not get to within the timeframe? Feel free to discuss those here as well.
