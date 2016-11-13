# Rails as an API Study

Use your favorite search engine and the provided readings to research and answer
the following questions (no prior knowledge is expected).

In your answers, be sure to cite any relevant sources you consulted in your
search. We ask you to write answers in your own words in order to see how you
process what you've read. Please do not answer with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [rails-api-template](https://github.com/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   [Starting Ruby on Rails: What I Wish I Knew | BetterExplained](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
-   [Intermediate Rails: Understanding Models, Views and Controllers | BetterExplained](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)
-   [The Rails Command Line — Ruby on Rails Guides](http://guides.rubyonrails.org/command_line.html)
-   [Rails Routing from the Outside In — Ruby on Rails Guides](http://guides.rubyonrails.org/routing.html)
-   [Action Controller Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/action_controller_overview.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
The model layer is Ruby classes, it's what talks to the database. This is
where you store and validate data.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
Controllers do the work of parsing user requests, data submissions, cookies, sessions and the “browser stuff”. It gives orders to specific tasks regardless of how tasks are accomplished.
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
The Rails router recognizes URLs and releases them to a controller's action. It can also generate paths and URLs, avoiding the need to hardcode strings in your views.
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
The client makes a GET request to a specific URL.
The web server receives the GET request.
The web server checks the routes file to determine the controller action.
The web server uses dispatch to create a new controller and call the action.
The controller action parses the request and requests info from the model.
The model performs the business logic and gets data from the DB as needed.
The model sends the information back to the controller.
The controller requests the presentation from the View.
The view sends the presentation information back to the controller.
The controller returns the response body back to the web server.
The web server passes the request back to the client.
```
