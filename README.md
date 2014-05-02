# owning-a-home

[![Build Status](https://travis-ci.org/cfpb/owning-a-home.svg?branch=master)](https://travis-ci.org/cfpb/owning-a-home)

## This project is a work in progress. 
Nothing presented in the issues or in this repo is a final product unless it is marked as such or appears on www.consumerfinance.gov/owning-a-home. Some copy or formulas may be replaced with dummy text to ensure that we follow any and all privacy and security procedures at the CFPB. All the designs, layouts, and evolution of our decision making process are accurate. 

## We want your feedback, but will not be able to respond to everyone.
We are working under an agile framework, and plan to use this repo to publish, receive feedback, and iterate on that feedback as often as possible. Our goal is to see user trends and reactions to our work. We want as much feedback as possible to help us make informed decisions so that we can make this tool better. Unfortunately, we will not be able to respond to every piece of feedback or comment we receive, but intend to respond with our progress through the evolution of the tool.

## Requirements

- [Sheer](https://github.com/rosskarchner/sheer)
- [Elasticsearch](http://www.elasticsearch.org/)
- [Node](http://nodejs.org/)
- [Grunt](http://gruntjs.com/)
- [Bower](http://bower.io/)

## Getting up and running with sheer

[Sheer](https://github.com/rosskarchner/sheer) is "A Jekyll-inspired, elasticsearch-powered, CMS-less publishing tool."

To get started with Sheer:

Install [Elasticsearch](http://www.elasticsearch.org/) however you'd like. (we use [homebrew](http://brew.sh/))::

```
$ brew install elasticsearch
```

Check out the sheer Github project:
```
$ git clone https://github.com/rosskarchner/sheer.git
```

create a virtualenv for sheer:
```
$ mkvirtualenv sheer
```

The new virtualenv will activate right away. to activate it later on (say, in a new terminal session) use the command "workon sheer"

Install sheer into the virtualenv with the -e flag (which allows you to make changes to sheer itself):

```
$ pip install -e ~/path/to/sheer
```

Install sheer's python requirements:

```
$ pip install -r ~/path/to/sheer/requirements.txt
```

You should now be able to run the sheer command:
```
$ sheer

usage: sheer [-h] [--debug] {inspect,index,serve} ...
sheer: error: too few arguments
```

## Running owning-a-home

Clone this repo, `cd` to it, and run:

```
$ sheer index . 
```

This loads all of the *content* into elasticsearch

To look at the resulting site, run:

```
$ sheer serve .
```

And browse to http://localhost:7000

## Working with the front-end.

The owning-a-home front-end currently uses the following:

- [LESS](http://lesscss.org/)
- [Capital Framework](http://cfpb.github.io/capital-framework/)
- [Grunt](http://gruntjs.com/)
- node/CommonJS style modules (compiled with [Browserify](http://browserify.org/))
- [Bower](http://bower.io/) & [npm](https://www.npmjs.org/) for package management

### Installing Dependencies

Install [node.js](http://nodejs.org/) however you'd like. (we use [homebrew](http://brew.sh/)):

```
$ brew install node
```

Install [Grunt](http://gruntjs.com/), a JavaScript task runner:

```
$ npm install -g grunt-cli
```

Install the dependencies with npm and the custom `grunt vendor` task:

```
$ npm install
$ grunt vendor
```

### Developing

We use [Grunt](http://gruntjs.com/) to compile and compress our Less and JavaScript files. The easiest way to do that is to run the `watch` task. This will watch for changes and run grunt whenever you save a file:

```
grunt watch
```

## Contributions.
We welcome contributions, in both code and design form, with the understanding that you are contributing to a project that is in the public domain, and anything you contribute to this project will also be released into the public domain. See our [CONTRIBUTING file](https://github.com/cfpb/owning-a-home/blob/master/CONTRIBUTING.md) for more details.
