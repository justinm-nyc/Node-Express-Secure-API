# Contacts API



### Open a terminal window in the root folder
``` bash
# Install dependencies:
npm install

# Start the application:
npm start

```

Register a user by sending a POST request to http://localhost:3000/auth/register with a username, email, and password in the body and with 'Content-Type' as application/x-www-form-urlencoded in the Headers.

Login to a user account by sending a POST request to http://localhost:3000/auth/login with a username, email, and password in the body with 'Content-Type' as application/x-www-form-urlencoded in the Headers. You will be returned a JWT token. 


To create a contact, send a POST request to http://localhost:3000/contact
with a firstName and lastName values in the body and with 'Content-Type' as application/x-www-form-urlencoded in the Headers. Also add an 'Authorization' key and as the value put 'JWT {{JWT token from login}}'.

To query for all contacts, send a GET request to http://localhost:3000/contact with 'Content-Type' as application/x-www-form-urlencoded in the Headers. Also add an 'Authorization' key and as the value put 'JWT {{JWT token from login}}'.

To query for a specific contact, send a GET request to http://localhost:3000/contact/{{ contactId }} with the contact id in the endpoint and with 'Content-Type' as application/x-www-form-urlencoded in the Headers. Also add an 'Authorization' key and as the value put 'JWT {{JWT token from login}}'.