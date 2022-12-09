# Final

Task 1

In order to access external REST APIs, for this assignment, you must use the requests package to communicate in the HTTP protocol.

Finish the implementation of the class called AccessApi. There are 7 method stubs that will need to be completed:

A constructor that requires the developer to input a base URL as a string that will host the REST API endpoint. Example: “http://google.com”
A method to get the current URL base.
A method to set the current URL base.
A method to test if the URL is responding to GET requests to allow for a simple alive test.
A method to input an endpoint, as a string, and have that endpoint concatenated to the base URL and then send a GET request using the requests package to the combined URL. Then, return the JSON sent as a list.
A method to input an endpoint and have that endpoint concatenated to the base URL and then send a GET request using the requests package to the combined URL. Then, return the status code.
A method to input an endpoint and have that endpoint concatenated to the base URL and then send a GET request using the requests package to the combined URL. Then, return the total elapsed time used for the GET request.

-------------------------------------------------------------------------------------
Task 2

Now that the AccessApi class has been created, we must create tests for each of the API endpoints.

Schema’s of response JSON’s

getBillingInfo.json

  "id": < INT>,
  "FirstName": <STRING>,
  "LastName": <STRING>,
  "city": <STRING>,
  "state": <STRING>,
  "Lang": <STRING>,
  "SSN":<STRING>
getCustomers.json

"id": < INT>,
"first_name": <STRING>,
"last_name":<STRING>,
"email":<STRING>,
"ip_address":<STRING>,
"address": <STRING>
getSites.json

"id": <INT>,
"address": <STRING>,
"ThirdParty":<STRING>,
"admin": <STRING>
In the file test_company_api.py, you will find test method stubs. Create the following four tests for each of the API endpoints:

Validate the HTTP status code is 200.
Validate the schema matches the one provided on a very simple level. Determine that the JSON keys are correct. For example, in getSites check that there are 4 keys: id, address, ThirdParty and admin. Also check that the type of the value matches the schema provided. A schema is the layout of the data, which could be columns in a spreadsheet or key’s and nested key’s in a dictionary. To validate the schema, you would verify that the structure matches what is expected.

Validate the accuracy of the data by picking a random data element and verifying the data is in the correct format. For example, a SSN should be all integers, in a format of XXX-XX-XXXX.

Validate that the response time should be less than one minute.
Endpoints:

• Billing

• Sites

• Customers

The JSON files can be found here. For now, please use: https://raw.githubusercontent.com/cengage-ide-content/ as the base URL. For example https://raw.githubusercontent.com/cengage-ide-content/APItesting/main/getBillingInfo.json.

A simple pytest looks like as follows:

def <test_name>(<args>):                  
    <setup code for test>
    assert <an expression that tests and has a True or False outcome>
A simple example is as follows:

def testing_my_class(age:int):
    assert age <= 50              
