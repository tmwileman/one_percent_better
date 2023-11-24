Current Streak: 4 
All Time Best Streak: 4

# AWS API Gateway
#Tags: #ComputerScience #AWS #APIGateway 

# What is an API
APIs can be thought of as waiters in a restaurant. They take orders from customers in the front and communicate those orders to the kitchen in the back. They then return to the customer with a meal. 

Application Programming Interfaces (APIs) are similar to the waiter but for computer programs. APIs help different computer programs talk to each other. For example, when you use a weather app on your phone, the app uses an API to get weather information from a computer somewhere that is keeping track of all the weather information and then brings it back to your phone app. You don't have to go to the big weather computer yourself. You can just send a request and get a response for your particular area.

In short, APIs enable efficient communication between programs so we can easily access information. 

# RESTful APIs
REpresentational State Transfer (REST) APIs is a fancy way of saying that an API uses simple, predictable commands (like GET, POST, PUT, or DELETE) to send small messages to other programs to ask for data for tell it to do something. 

An example is your social media app o fchoice. This app uses a RESTful API to get the lastest messages from a server. It sends a request that says "GET the latest messages", and the app's server understands what is wanted and sends the information back.

# WebSocket APIs
Think of WebSocket APIs like walkie-talkies but for computer programs. Normally, using the internet is like sending letters: you send a request and then get a response. This is how traditional web requests like loading a webpage work. But if you wnat to have a real-time conversation, or keep up with a live event, these messages would be too slow. 

This is where WebSocket APIs come in. They create a two-way communication line between your device and a server. Once the line is open, either side can send data to the other immediately, without waiting. Both the server and device can talk whenever they want without having to send individual messages. 

# What is AWS API Gateway
API Gateway is a service that acts like a traffic controller for applications. It makes creating, publishing, maintaining, monitoring, and securing APIs easier. 