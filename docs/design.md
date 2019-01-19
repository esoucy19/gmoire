Design decisions regarding the application are detailed here.

# Project methodology

## Twelve Factor App

I will try to apply the Twelve Factor App principles. In particular, I'll want
to make sure the environment I develop and test in is as close to the
environment I envision for production as possible.

## Environment

### Dev / testing

I will be developping / testing on a Docker image of Debian. A simple testing
script and Dockerfile might be enough to begin with, but if testing ends up
getting more complex and requiring more setup I'm not opposed to using Test
Kitchen to manage the testing environment.

### Production

I want to use Debian Stable as a base to host the application. Still not certain
if I want to do it on a plain Debian server or using Docker. I have no
experience with Docker Compose / Docker Swarm and such but I'd be willing to try
them out.

#### Hosting

If I ever want to make the application publicly available I'll probably host it
on Linode or Digitalocean. If I'm mostly using it for myself I should make sure
to shut it down when not using it so I don't end up paying too much for it.
Maybe those companies have special rates for open source projects? Also if I use
a public cloud instance I might use it to host some other personal stuff or
projects to save money.

## Test-driven development (TDD)

I want to use Cucumber for integration / acceptance testing and pytest for
unit testing. I'll be using Behave, the most popular Cucumber library for
Python.

I keep wanting to use TDD for my projects and I'm still not that great at it,
so it's definitely something to work on.

### Outside-In TDD

I'll try to work with an Outside-In TDD model. Basically that means I'll focus
on delivering specific "customer-facing" features based on user stories. This
method forces you to get an actual working prototype working as soon as
possible. It also ensures you don't end up working on backend features you're
not using. Until proven otherwise I'm my own target customer but the exercise
remains useful.

# Structure outline

Currently I am leaning towards keeping the application as simple as possible, as
it is also a personal learning project.

## Programming language

I'll be using Python 3 as the main language for the project. It's the language I
know most about and it has good facilities for web development. If I can make
the app modular enough that I can incporporate modules in other languages I'm
learning or interested in, then all the better, although that's not a
pre-requisite right now.

### Python version

I'll be using Python 3.6 for the project. It's fairly recent and can be used on
most platforms without too much work.

I'll be using Pyenv to manage Python versions and Pipenv to manage packages and
virtualenvs. I'm used to them and they work well enough for me.

## Back end

### Web framework

I prefer small / minimal frameworks for I opted for using Flask for this
project. Flask will allow me to start small and use only the features I need and
add more stuff later on as needed.

### Database

Still not 100% sure on the Database I'll be using. I am currently leaning
towards PostgresSQL because it is a good default with a lot of support
resources, but a document DB or even Graph DB wouldn't be out of question if I
feel like learning one of those.

## Front end

I want to keep the front end as simple as possible to begin with, with plans to
probably expand it once I have a working base going.

### HTML / templating engine

Still wondering if I'll use an HTML alternative (does Python have a haml / pug
equivalent?)

I will definitely be using jinja2 as the main templating language as it's the
one I'm most used to.

### CSS

I will start out with some plain, simple CSS. Eventually I'll probably want to
use a CSS pre-procesor. What's popular now? Less or Sass? Will have to look it
up when it becomes relevant.

Will probably want to use a CSS framework at some point. Bootstrap would
probably be the easiest choice. Maybe even use a template. Maybe look up a
smaller framework?

### Javascript

No JS or only minimal JS to begin with. I don't think I'll want to use a big
JS Framework. Maybe use a minimal one for some stuff, like Ember or Vue or
even just Underscore or JQuery?
