# Reading: API Integration

## Dynamic API Server
An Express/Node.js based server designed to be a “model agnostic” REST API server, which can perform (CRUD) operations on any data model.

## Support all REST/HTTP methods:

GET: Retrieve record(s) from a data source (All, One (by id), Some (by filtering)).
POST: Create a new record in a data source.
PUT: Update a single full record in a data source.
PATCH: Update part of a single record in a data source.
DELETE: Delete a record in a data source.


## Technical Requirements For Server
The application will be created with the following overall architecture and methodologies

Node.js

ES6 Classes and best practices

ExpressJS Web Server, built modularly

“Auth” routes for handling the login and authentication system
POST /signup to create an account
POST /signin to login with Basic Auth
GET /oauth
Middleware for handling 404 and 500 conditions
Middleware for handling each type of authentication
Basic (username + password) to be used on the /signin route only
i.e. app.post('/signin', basicAuthentication, (req, res) => { ... })
OAuth (3rd Party) to be used on the /oauth route only
i.e. app.get('/oauth', OAuth, (req, res) => { ... })
Handles the handshake process from a 3rd party OAuth system
Bearer (token) to be used on any other route in the server that requires a logged in user
i.e. app.get('/secretstuff', tokenAuthentication, (req, res) => { ... })
Middleware for handling authorization
To be run after Bearer Middleware on routes to be protected
Accepts a “capability” as a parameter
i.e. app.delete('/secretstuff', tokenAuthRequired, capability('delete'), (req, res) => { ... })
User Persistence using a Mongo Database (NoSQL)
Mongoose Schemas (data models) to define and model data
Test Driven Development, using Jest
Tests will be runnable locally
Tests will auto-execute (CI) in your repo using GitHub actions
Tests will use a 3rd party library called supergoose to:
“mock” the mongo running database
“mock” the running Express server
Deployment to Heroku