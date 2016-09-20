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
The model interacts with the database (probably using SQL commands) to both represent and store the data for the rest of the framework.  It talks to the controller about the data it contains/represents.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The controller servers as the go-between for the model and the view.  It coordinates between the view and the model, taking data from the model and sending it to be represented by the view.  They also handle authorization concerns (user login/authentification/session data).  The controller also collects data from the user and sends it to the model for storage/manipulation.
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
The router decides which controller to send input from the user, based upon URLs, which usually correspond to the particular controller for the action in question.  Routing simplifies creating standard HTTPS actions/URLs to specific controllers (which have actions).
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
The client sends a request (a GET in this case) using a browser.  The router receives this request and provides the URL corresponding to the controller needed to handle the request.  The controller then provides a specific action for the request and sends it to the view, which renders the HTML and sends it back to the controller.  The controller presents it to the browser which paints it to the screen so the user can interact with it.
```
