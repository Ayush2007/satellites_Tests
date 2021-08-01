Steps to run test :

1. Install node
2. install postman and import the package with environment variables
3. Run collection

Note Global Variables :

variable = url
Initial value = https://api.wheretheiss.at/v1/satellites/25544
Current value = https://api.wheretheiss.at/v1/satellites/25544

Issues found :

satellites/[id]/positions :

1.timestamps limit of 10 per request is not applicable, and it accepts more than 10 timestamps in the request, which should throw and error


2. units other than miles and kilometers are accepted and no error is thrown


satellites/[id]/tles


1. format other than JSOn and text when passed in request doesn't give any error response



Improvements :
- error code for unexpected formats and units

- more than 10 max timestamp rule should be checked

- different combinations of error code should be validated with requests, such as internal server error codes




