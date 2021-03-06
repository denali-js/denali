# Denali

[![CircleCI](https://img.shields.io/circleci/project/github/denali-js/core.svg?style=flat-square)](https://circleci.com/gh/denali-js/core)
[![Coverage](https://img.shields.io/codeclimate/coverage/github/denali-js/core.svg?style=flat-square)](https://codeclimate.com/github/denali-js/core)
[![Dependencies](https://img.shields.io/david/denali-js/core.svg?style=flat-square)](https://david-dm.org/denali-js/core)
[![npm downloads](https://img.shields.io/npm/dm/@denali-js/core.svg?style=flat-square)](https://www.npmjs.com/package/@denali-js/core)
![latest version](https://img.shields.io/npm/v/@denali-js/core.svg?style=flat-square)

> An opinionated Node framework for building robust JSON APIs

Denali is a tool to help you build and deliver amibitous JSON APIs. It features:

 * First class JSON serializers, including out of the box JSON-API support
 * A single controller class (called Actions) per endpoint
 * Flexible, declarative filter system
 * An emphasis on developer happiness - a robust CLI, powerful testing primitives,
   and support for the full lifecycle of app development
 * ORM-agnostic design - choose your favorite Node ORM, or none at all

## Why Denali?

Denali should feel familiar to anyone who has worked with popular MVC frameworks
like Rails. But Denali has a slightly unique take on each aspect of the MVC
pattern:

### (M)VC - ORM Adapters instead of ORM lock-in

Unlike many server frameworks, Denali lets you choose which ORM you'd like to
use. ORMs are hard, and the Node ecosystem has multiple competing options, each
with it's own strengths and weaknesses. Rather than limiting you to a single
"official" ORM, or worse, attempting to roll our own, Denali uses an adapter
system to ensure that whatever ORM you bring, it can work with the Denali
ecosystem.

### M(V)C - Serializers instead of Views & Templates

Denali's view layer is unique as well. Rather than traditional HTML rendering,
Denali's view layer renders JSON. Instead of the usual templates and view
classes, we have Serializers instead, which tell Denali how to render the data
you supply as a response. The separation of responsibilties ensures you can
tweak how your data is structured in your API without having to change any of
the logic of your app. Several common formats, including JSON-API, are supported
out of the box, and customization is easy.

### MV(C) - Actions instead of Controllers

In Denali, the Action class takes the role of the controller in the application.
But rather than a single controller class that responds to many different
endpoints, an Action class is responsible for responding to requests against
a single endpoint (URL + method) only. The result is powerful - since the Action
class directly and completely represents the app's response handler, we can use
expressive declarative syntax to succinctly define behaviors.

## Getting Started

You can install Denali globally via npm:

```sh
$ npm install -g denali denali-cli
```

Create a new application (run with Node 6.0+):

```sh
$ denali new my-api
$ cd my-api
```

You can use the `server` command to run your API locally in development mode.
The API server will automatically restart when you make a change:

```sh
$ denali server
```

To learn more, check out [the docs](http://denalijs.org/) or join us on [Slack](https://denali-slack.now.sh/)

## License

MIT © [Dave Wasmer](http://davewasmer.com)
