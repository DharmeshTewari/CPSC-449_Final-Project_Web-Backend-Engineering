# Final Project - Cloud Service Access Management System with MongoDB, Postman, and PyCharm: Dynamic access control, subscription management, and usage tracking for cloud APIs.

## Team Members:
1- Dharmesh Tewari
2- Jahanvi Paliwal
3- Viraat Udar

## Steps to run the application:
1.	create environment and activate.
2.	run command "pip install -r requirements.txt" to install all dependencies.
3.	run command py main.py to run the application.
4.	test through postman on http://localhost:8001/*.


## API Details:

The code defines the following APIs:
1.	Create Plan API
•	Method: POST
•	Path: "/plans"
•	Description: Create a new subscription plan.

2.	Get All Plans API
•	Method: GET
•	Path: "/plans"
•	Description: Retrieve details of all subscription plans.

3.	Modify Plan API
•	Method: PUT
•	Path: "/plans/{plan_id}"
•	Description: Modify details of a specific subscription plan.

4.	Delete Plan API
•	Method: DELETE
•	Path: "/plans/{plan_id}"
•	Description: Delete a specific subscription plan.

5.	Add Permission API
•	Method: POST
•	Path: "/permissions"
•	Description: Add a new permission.

6.	Get All Permissions API
•	Method: GET
•	Path: "/permissions"
•	Description: Retrieve details of all permissions.

7.	Modify Permission API
•	Method: PUT
•	Path: "/permissions/{permission_id}"
•	Description: Modify details of a specific permission.

8.	Delete Permission API
•	Method: DELETE
•	Path: "/permissions/{permission_id}"
•	Description: Delete a specific permission.

9.	Subscribe to Plan API
•	Method: POST
•	Path: "/subscriptions"
•	Description: Subscribe to a specific plan.

10.	Get Subscription Details API
•	Method: GET
•	Path: "/subscriptions/{user_id}"
•	Description: Retrieve subscription details for a specific user.

11.	Assign/Modify User Plan API
•	Method: PUT
•	Path: "/subscriptions/{user_id}"
•	Description: Assign or modify the subscription plan for a specific user.

12.	Check Access Permission API
•	Method: GET
•	Path: "/access/{user_id}/{api_request}"
•	Description: Check if a user has access permission for a specific API request.

13.	Track API Request API
•	Method: POST
•	Path: "/usage/{user_id}"
•	Description: Track an API request made by a user.

14.	Check Limit Status API
•	Method: GET
•	Path: "/usage/{user_id}/limit"
•	Description: Check the usage limit status for a specific user.
