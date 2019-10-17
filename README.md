# Node Express Secure API with JSON Web Tokens
An API for registering a user, logging in, and querying contacts that is secured using JSON Web Tokens. 

## Start Application
### Open a terminal window in the root folder
``` bash
# Install dependencies:
npm install

# Start the application:
npm start

```

## Use Application
### Register A user
Register a user by sending a POST request to http://localhost:3000/auth/register with a username, email, and password in the body and with 'Content-Type' as application/x-www-form-urlencoded in the Headers.

### Login To User Account
Login to a user account by sending a POST request to http://localhost:3000/auth/login with a username, email, and password in the body with 'Content-Type' as application/x-www-form-urlencoded in the Headers. You will be returned a JWT token. 

### Create A Contact
To create a contact, send a POST request to http://localhost:3000/contact
with a firstName and lastName values in the body and with 'Content-Type' as application/x-www-form-urlencoded in the Headers. Also add an 'Authorization' key and as the value put 'JWT {{JWT token from login}}' with the JWT token in the value.

### Query All Contacts
To query for all contacts, send a GET request to http://localhost:3000/contact with 'Content-Type' as application/x-www-form-urlencoded in the Headers. Also add an 'Authorization' key and as the value put 'JWT {{JWT token from login}}'.

### Query For Specific Contact
To query for a specific contact, send a GET request to http://localhost:3000/contact/:contactId with the contact id in the endpoint and with 'Content-Type' as application/x-www-form-urlencoded in the Headers. Also add an 'Authorization' key and as the value put 'JWT {{JWT token from login}}'.