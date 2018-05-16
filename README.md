# Things Learned About Ruby on Rails

## Rails Philosophy

Rails is a web framework that was built to allow developers to spend less time on trivial things, but instead on the big picture. It comes with a set of assumptions that comes pre-defined so that you can perform very little work, but get a large result from. 

In a similar vein, Ruby is a language that allows developers to be very productive as well. I think it tries very hard to look like English: it uses very little amounts of punctuation (curly braces, brackets) and instead has word-based lexicons within the language. The language also comes with a very complete standard library that takes care of many, many operations.

## Model View Controller (MVC)

MVC is an architecture for building Web applications that allow for the developer to have separate sections of code that is split into their respective responsibilities.

This separation of code allows for code modularity so that one can easily reuse code from another block, and because the code is separated by their responsibilities, the code is naturally quite modular

### Model

The Model is the part of the code that defines the Data Structure of the the data of interest. It is responsible for dealing with the Database. An important thing to note is that although the View and Controller and technically be inter-mixed together, the Model is always independent of the View and Controller

### View

The View is the part of the code that defines how the Web application should look, given the Behavior from the Controller, and the Data from the Model. For example, ReactJS is a purely View library. It uses data from elsewhere (Model), and depending on the URL, (React-router/REST-API/Controller), it renders a View

### Controller

The Controller is the part of the code that does a lot of the heavy lifting in Ruby on Rails. It is the part of the code that resembles ExpressJS in NodeJS development, where you would define what kind of data from the model should be passed into what route. This should not be confused with the role that `config/routes.rb` assumes because the `routes.rb` file is responsibile for the actual route/url that the user of the web application is on, but the Controller is responsible for what data should be passed when the user does some operation within that url/route

## Specific Tidbits

1. According to Traversy Media, it is a good practice to name Models starting with a Capital letter as a singular word, like "Post", or "Data"

    - On the other hand, Controllers should be the capital, plural version of the Same word, ie: "Posts", "Datas"

2. If you have a Controller that should uses most/all CRUD operations and you need to define their routes in `config/routes.rb`, defining the controller as a resource automatically creates the routes using a set of assumptions that Rails was built on.


