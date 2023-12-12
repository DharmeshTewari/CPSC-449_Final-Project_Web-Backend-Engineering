# CPSC-449_Final-Project_Web-Backend-Engineering
Cloud Service Access Management System with MongoDB, Postman, and PyCharm: Dynamic access control, subscription management, and usage tracking for cloud APIs.

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cloud Service Access Management System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }

        h1, h2, h3 {
            color: #333;
        }

        ul, ol {
            margin-bottom: 20px;
        }

        li {
            margin-bottom: 10px;
        }

        a {
            color: #007BFF;
        }

        code {
            background-color: #f8f9fa;
            border: 1px solid #e1e4e8;
            border-radius: 3px;
            font-family: SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
            padding: 3px 5px;
        }

        pre {
            background-color: #f8f9fa;
            border: 1px solid #e1e4e8;
            border-radius: 3px;
            padding: 10px;
            overflow: auto;
        }

        ol ol {
            list-style-type: lower-alpha;
        }

        ol ol ol {
            list-style-type: lower-roman;
        }
    </style>
</head>

<body>

    <h1>Final Project - Cloud Service Access Management System</h1>
    <h2>with MongoDB, Postman, and PyCharm: Dynamic access control, subscription management, and usage tracking for cloud APIs.</h2>

    <h2>Team Members:</h2>
    <ul>
        <li>Dharmesh Tewari</li>
        <li>Jahanvi Paliwal</li>
        <li>Viraat Udar</li>
    </ul>

    <h2>Steps to run the application:</h2>
    <ol>
        <li>Create environment and activate.</li>
        <li>Run command <code>pip install -r requirements.txt</code> to install all dependencies.</li>
        <li>Run command <code>py main.py</code> to run the application.</li>
        <li>Test through postman on <a href="http://localhost:8001/*">http://localhost:8001/*</a>.</li>
    </ol>

    <h2>API Details:</h2>

    <p>The code defines the following APIs:</p>

    <ol>
        <li><strong>Create Plan API</strong></li>
        <ul>
            <li>Method: POST</li>
            <li>Path: "/plans"</li>
            <li>Description: Create a new subscription plan.</li>
        </ul>

        <li><strong>Get All Plans API</strong></li>
        <ul>
            <li>Method: GET</li>
            <li>Path: "/plans"</li>
            <li>Description: Retrieve details of all subscription plans.</li>
        </ul>

        <li><strong>Modify Plan API</strong></li>
        <ul>
            <li>Method: PUT</li>
            <li>Path: "/plans/{plan_id}"</li>
            <li>Description: Modify details of a specific subscription plan.</li>
        </ul>

        <li><strong>Delete Plan API</strong></li>
        <ul>
            <li>Method: DELETE</li>
            <li>Path: "/plans/{plan_id}"</li>
            <li>Description: Delete a specific subscription plan.</li>
        </ul>

        <li><strong>Add Permission API</strong></li>
        <ul>
            <li>Method: POST</li>
            <li>Path: "/permissions"</li>
            <li>Description: Add a new permission.</li>
        </ul>

        <li><strong>Get All Permissions API</strong></li>
        <ul>
            <li>Method: GET</li>
            <li>Path: "/permissions"</li>
            <li>Description: Retrieve details of all permissions.</li>
        </ul>

        <li><strong>Modify Permission API</strong></li>
        <ul>
            <li>Method: PUT</li>
            <li>Path: "/permissions/{permission_id}"</li>
            <li>Description: Modify details of a specific permission.</li>
        </ul>

        <li><strong>Delete Permission API</strong></li>
        <ul>
            <li>Method: DELETE</li>
            <li>Path: "/permissions/{permission_id}"</li>
            <li>Description: Delete a specific permission.</li>
        </ul>

        <li><strong>Subscribe to Plan API</strong></li>
        <ul>
            <li>Method: POST</li>
            <li>Path: "/subscriptions"</li>
            <li>Description: Subscribe to a specific plan.</li>
        </ul>

        <li><strong>Get Subscription Details API</strong></li>
        <ul>
            <li>Method: GET</li>
            <li>Path: "/subscriptions/{user_id}"</li>
            <li>Description: Retrieve subscription details for a specific user.</li>
        </ul>

        <li><strong>Assign/Modify User Plan API</strong></li>
        <ul>
            <li>Method: PUT</li>
            <li>Path: "/subscriptions/{user_id}"</li>
            <li>Description: Assign or modify the subscription plan for a specific user.</li>
        </ul>

        <li><strong>Check Access Permission API</strong></li>
        <ul>
            <li>Method: GET</li>
            <li>Path: "/access/{user_id}/{api_request}"</li>
            <li>Description: Check if a user has access permission for a specific API request.</li>
        </ul>

        <li><strong>Track API Request API</strong></li>
        <ul>
            <li>Method: POST</li>
            <li>Path: "/usage/{user_id}"</li>
            <li>Description: Track an API request made by a user.</li>
        </ul>

        <li><strong>Check Limit Status API</strong></li>
        <ul>
            <li>Method: GET</li>
            <li>Path: "/usage/{user_id}/limit"</li>
            <li>Description: Check the usage limit status for a specific user.</li>
        </ul>
    </ol>

    <h2>Testing API:</h2>

    <ol>
        <li>Start MongoDB:</li>
        <ul>
            <li>Ensure that your MongoDB server is running.</li>
        </ul>

        <li>Open PyCharm:</li>
        <ul>
            <li>Open PyCharm IDE on your computer.</li>
        </ul>

        <li>Open Project:</li>
        <ul>
            <li>Open the Cloud Service Access Management System project in PyCharm.</li>
        </ul>

        <li>Run the FastAPI Application:</li>
        <ul>
            <li>Run the FastAPI application by executing the main.py script.</li>
            <li>Verify that the application is running without errors.</li>
        </ul>

        <li>Insert Default Sample Data:</li>
        <ul>
            <li>Check if the default sample data is inserted successfully by looking for the "Default sample data inserted successfully" message in the console.</li>
        </ul>

        <li>Open Postman:</li>
        <ul>
            <li>Open the Postman application on your computer.</li>
        </ul>

        <li><strong>Create Plan:</strong></li>
    <ul>
        <li>Use Postman to create a new plan by sending a POST request to <code>http://127.0.0.1:8001/plans</code> with a JSON body containing plan details.</li>
        <li><strong>Example JSON Body:</strong></li>
        <pre>
{
 "plan_name": "Silver Plan", 
"description": "Moderate access", 
"api_permissions": ["api1", "api3"], 
"usage_limits": {"api1": 200, "api3": 100}
}
        </pre>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "Plan created successfully",
    "plan_id": "Generated Plan ID"
}
        </pre>
    </ul>

    <li><strong>Get All Plans:</strong></li>
    <ul>
        <li>Retrieve all plans using Postman by sending a GET request to <code>http://127.0.0.1:8001/plans</code>.</li>
        <li>Verify that the newly created plan is listed.</li>
    </ul>

    <li><strong>Modify Plan:</strong></li>
    <ul>
        <li>Modify the plan using Postman by sending a PUT request to <code>http://127.0.0.1:8001/plans/{plan_id}</code> with the updated plan details.</li>
        <li><strong>Example URL:</strong></li>
        <pre>
http://127.0.0.1:8001/plans/{plan_id}
        </pre>
        <li><strong>Example JSON Body:</strong></li>
        <pre>
{
 "plan_name": "Silver Plan", 
"description": "Moderate access", 
"api_permissions": ["api1", "api3", "api5"], 
"usage_limits": {"api1": 200, "api3": 100, "api5": 50} 
}
        </pre>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "Plan modified successfully"
}
        </pre>
    </ul>
<li><strong>Delete Plan:</strong></li>
    <ul>
        <li>Delete the plan using Postman by sending a DELETE request to <code>http://127.0.0.1:8001/plans/{plan_id}</code>.</li>
        <li><strong>Example URL:</strong></li>
        <pre>
http://127.0.0.1:8001/plans/{plan_id}
        </pre>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "Plan deleted successfully"
}
        </pre>
    </ul>

    <li><strong>Subscribe to Plan:</strong></li>
    <ul>
        <li>Subscribe a user to a plan using Postman by sending a POST request to <code>http://127.0.0.1:8001/subscriptions</code> with a JSON body containing subscription details.</li>
        <li><strong>Example JSON Body:</strong></li>
        <pre>
{
 "user_id": "user456", 
"plan_id": "{plan_id}", // Use the ID of an existing plan 
"subscribed_at": "2023-01-01T12:00:00",
 "api_permissions": ["api1", "api3"] 
}
        </pre>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "Subscribed successfully",
    "subscription_id": "Generated Subscription ID"
}
        </pre>
    </ul>

    <li><strong>Check Access Permission:</strong></li>
    <ul>
        <li>Check access permission using Postman by sending a GET request to <code>http://127.0.0.1:8001/access/{user_id}/{api_request}</code>.</li>
        <li><strong>Example URL:</strong></li>
        <pre>
http://127.0.0.1:8001/access/user456/api1
        </pre>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "Access granted"
}
        </pre>
    </ul>

    <li><strong>Track API Request:</strong></li>
    <ul>
        <li>Track an API request using Postman by sending a POST request to <code>http://127.0.0.1:8001/usage/user456</code> with a JSON body containing usage details.</li>
        <li><strong>Example JSON Body:</strong></li>
        <pre>
{
 "user_id": "user456",
 "api_request": "/api1", 
"timestamp": "2023-01-01T12:15:00"
}
        </pre>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "API request tracked successfully"
}
        </pre>
    </ul>

    <li><strong>Check Limit Status:</strong></li>
    <ul>
        <li>Check the limit status using Postman by sending a GET request to <code>http://127.0.0.1:8001/usage/user456/limit</code>.</li>
        <li><strong>Expected Response:</strong></li>
        <pre>
{
    "message": "Within limit"
}
        </pre>
    </ul>
</ol>
<p>This script outlines the steps to demonstrate the key features of the Cloud Service Access Management System using PyCharm, MongoDB, and Postman. Adjust the details based on your specific implementation.</p>

