# Backend Microservice

A simple stateless microservice in Nodejs, with following functionalities -

 * Authentication
 * Image Thumbnail Generation


## Setup

The API requires:
  [Node.js](https://nodejs.org/en/download/)
  [Express](https://expressjs.com/)

Steps to run the project: 
    Clone the repo
    Go into the project directly and type npm install to install all the dependancies.
    Use npm start to run the app on port 3000
    You can change the "jwtPhrase" phrase to anything you want and try by crearting a new .env file in the project folder or updating the old file


## Testing the API routes.

### Authentication
This is a mock authentication so you can pass in any username or password to login.
 1. Set the request to **POST** and the url to _/api/users/login_. 
 2. In the **Body** for the Postman request, select **x-www-form-urlencoded**.
 3. You will be setting 2 keys (for username and password). Set the ```username``` key to any name. Set ```password``` to any password (minimum of 6 characters). Hit send to see the result which should contain username, authorized(Boolean) and JWT token.
 

### Image Thumbnail Generation
This request contains a public image URL. It downloads the image, resizes to 50x50 pixels, and returns the resulting thumbnail.
 1. Set the request to **POST** and the url to _/api/create-thumbnail_.
 2. Set the key ```imageUrl``` to a public image url.
 3. Since this is a secure route, for testing, you will have to set the token in the ```Header```. Set key as ```token``` and value as token you received from **Authentication**.
 4. Image will be downloaded and converted to a thumbnail of size 50x50 pixels with a sample result containing converted (Boolean), username, success message and path to the converted thumbnail.


