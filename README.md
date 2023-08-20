# bluebird-alif

Hi Bluebird, this is my submission to SQA Automation Engineer Test.

As it was stated, there is a JSON Object
{
    "order_id: "xxxxxx",
    "last_updated_timestamp": "1692525822",
    "driver_notes": "xxxxxx",
    "pickup_latitude": "xx.xxxx",
    "pickup_longitude": "xx.xxxx",
    "order_status": "xxx",
    "special_order": "xxx"
}

and there is an API that sent to /order and response with
{
    "last_updated_timestamp": "1692525822",
    "order_status": "xxx",
}

In this test, I have made as many assumptions to design the API Automation Framework.
1. The JSON Object can be accessed using CRUD, so in this repository I have tried to make sample/mock request for CRUD
2. The response that contained last_updated_timestamp and order_status is a GET Method. So in this sample repositories I have included them as a GET Request Method.
3. In all of the request, The Request's Query and Body is just my assumptions to make the API work as it should.
4. order_id is using GUID format
5. order_status have "completed" status
6. To update order, PATCH method is used

Then, based on the assumptions, I have made the project for API Automation in api/order.
To make things simple while still being easy to maintained, I have not included many Keywords in this project.

I have added:
- Test Cases
- Object Repository
- Test Suites
- Test Suites Collection
- Data Files
- Test Data
- "Orders" Keyword

In all of the folders, I add "Order" Folder. The idea is to make the repository more tidy based on the API URL.\
Inside The Test Case Folder /Order, I divided into methods that the API have. This will divide based on the methods and make it more tidy.\
The Data Files used an excel format (.xls), I have stored it in Test Data folder. It can be used based on sheet on different method of test cases.\
To run, I have divided Test Case, Test Suite, and Test Suite Collection. Test Case can be run individually. Test Suite will be run based on the URL of the API. Test Suite Collection is for the full regression of all APIs.\
The report used the basic Katalon Reports.\

For the validation of each requests I added verify the Status Code and JSON Schema.\

All of the "Orders" cannot be run, since it does not hit to actual API. To try Run the Test Case, Try Run User/Get User/POS01-get_user_by_page I used reqres.in for mocking this test case.

Thank you very much.