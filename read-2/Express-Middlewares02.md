# Express REST API

## **classes**

The clsaa it's another way to write object we were write the object ,
by use function the classes called special function and the classes in js bult on portotype ,

the class syntax has tow componenets ***class expression*** and ***class decleration*** .

***class expression:*** it's old way to define the syntax a class in ECMAScript 2015,
the class can be named or unnamed if named , the name of class is local the class body.

```
const Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  area() {
    return this.height * this.width;
  }
};

```


**class deleration:** The class declaration creates a new class with a given name using prototype-based inheritance.

```
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```

## **Using Express Routing**

**Routing** refers to how an application’s endpoints (URIs) respond to client requests.

you defin rouring by useing method of app for example we used the ```app.get()``` to get handl get requests  
and ```app.post()``` t handle post rquestsand ```app.use()``` to specify middleware as the callback function

## **Route methods**

```
// GET method route

app.get('/', (req, res) => {
  res.send('GET request ')
})

// POST method route

app.post('/', (req, res) => {
  res.send('POST request')
})

//PUT method route
app.put('/user', (req, res) => {
  res.send('Got a PUT request at /user')

//DELETE method route

  app.delete('/user', (req, res) => {
  res.send('Got a DELETE request at /user')
})
```
[To read more about the route](https://expressjs.com/en/guide/routing.html)

## **New Router in ExpressJS 4.0**

Express 4.0 comes with the new Router. Router is like a mini-Express application. It doesn’t bring in views or settings but provides us with the routing APIs like `use` ,`get`, `param`,`route` .

**express.Router( )** 

We can creat muliplie of routes  
```
router.get('/', function(req, res) {
        res.send('im the home page!');
    });
```

**Middleware router.use( )**
It'a the way to check somethin befor sent it to client like if this clien  authenticated or logging .


Here is some middleware to log a message to our console every time a request is made. This will be a demonstration of how to create middleware using the Express Router.
```

    // route middleware that will happen on every request
    router.use(function(req, res, next) {

        // log each request to the console
        console.log(req.method, req.url);

        // continue doing what we were doing and go to the route
        next();

        // apply the routes to our application
    app.use('/', router);
    });
```
 **Middleware for Parameters .prams( )**

 We will use Express’s .param() middleware. This creates middleware that will run for a certain route parameter. In our case, we are using :name in our hello route. Here’s the param middleware.


```

    // route middleware to validate :name
    router.param('name', function(req, res, next, name) {
        // do validation on name here
        // blah blah validation
        // log something so we know its working
        console.log('doing name validations on ' + name);

        // once validation is done save the new item in the req
        req.name = name;
        // go to the next thing
        next();
    });
```

**Login Routes app.route**
We can define our routes right on our app. This is similar to using `app.get`, but we will use` app.route`. app.route is basically a shortcut to call the Express Router. Instead of calling `express.Router()`, we can call app.route and start applying our routes there.

Using `app.route` lets us define multiple actions on a single login route. We’ll need a `GET` route to show the login form and a `POST` route to process the login form.


### **Conclusion**

With the inclusion of the Express 4.0 Router, we are given more flexibility than ever before in defining our routes. To recap, we can:

* Use `express.Router( )` multiple times to define groups of routes
* Apply the `express.Router()` to a section of our site using `app.use( )`
* Use route middleware to process requests
* Use route middleware to validate parameters using `.param()`
* Use `app.route()` as a shortcut to the Router to define multiple requests on a route