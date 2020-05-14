# Experience 2020 - API Best Practices
This repo provides the sample postman collection demonstrated during the **API Best Practices** session at the Ellie Mae Virtual Experience 2020.

**Prerequisites:**
	Postman software installation
	Developer Connect client id / secret
	Encompass credentials

## Setup 
1. Import Experience 2020 - API Best Practices.postman_collection.json 
l. Import Experience.postman_environment.json
1. Populate the Postman Environment with your developer connect client id / secret / Encompass credentials


## Running the Postman Collection

### Authentication
In order to test the API user postman, reach out to your Account Manager to request an API User key. Once this has been done, enter in the information to the api_user_client_id and api_user_client_secret environment variables.


### Lock and Concurrency
1. Add the Encompass credentials for two Encompass users to the smart_client_user, smart_client_user2, smart_client_password, smart_client_password2 environment variables
1. Find a test loan or create a new loan and retrieve the loan guid of the loan to enter into the loan_guid environment variable
1. Run the "00 - Get Security Token user1" and "00 - Get Security Token user2" requests to generate the access tokens for the two users 
1. You can now run each request in the Lock and Concurrency subfolders

### Webhooks
To test the webhooks collection, you will need to specify an endpoint for the webhook events to post to in the "Create Subscription" body. There are a few third party services that provide a way to view the webhook payload without having to host a publicly accessible endpoint that you could use to test out the webhook (e.g. webhook.site / requestbin.com)