## Event-Driven Programming in Node.js

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision. In this article we’re going to go over how Event-Driven Programming works and how we can make the best use of it in our Node.js projects.

#### **EventEmitter**

Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our project right away. Of course, creating our own version of EventEmitter wouldn’t be much of a challange, and in fact there are several modules published on npm such as EventEmitter2 and EventEmitter3 which promise a faster performance than the native EventEmitter.

```

const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;

```


- We want to alert everyone when a new user joins the chat room. We’ll need an event listener for a userJoined event.

```
const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;

function userJoined(username){
  // Assuming we already have a function to alert all users.
  alertAllUsers('User ' + username + ' has joined the chat.');
}

// Run the userJoined function when a 'userJoined' event is triggered.
chatRoomEvents.on('userJoined', userJoined);

```

#### **Removing Listeners**

To remove event listeners in EventEmitter we can use the `removeListener` or `removeAllListeners` method. It’s important to note that in the `EventEmitter`that comes built-in with Node you must pass a reference to the exact function you wish to remove when using the removeListener method


#### **Object Oriented Programming + Event-Driven Programming**

Imagine we’re building a mail application. We might have an object whose sole purpose is to process the incoming and outgoing mail messages for our client. This object would contain all of its own behavioral functions. We might have a sendMail function that delivers our mail to a server. We might also have a receiveMail function that tells the server to deliver us any new mail it has for us. We’ll call the object responsible for these server interactions our Mailbox.

```
const Mailbox = {
  sendMail: function(){
    // code to send mail.
  },
  receiveMail: function(){
    // check server for new mail.
  }
}

```
