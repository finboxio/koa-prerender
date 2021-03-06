# bot-koa-prerender

[![NPM](https://nodei.co/npm/bot-koa-prerender.png)](https://nodei.co/npm/bot-koa-prerender/)

**KOA middleware for prerendering javascript-rendered pages on the fly for SEO**

This [koa](https://koajs.com) middleware intercepts requests to your Node.js website from bots, and then makes a call to the (external)
[Prerender](https://prerender.io/) service to get the static HTML instead of the javascript for that page.

## Setup

### Prerequisites

Install [Prerender](https://github.com/prerender/prerender) on a server of your choice.

### Install

Install the [package](https://npmjs.org/package/bot-koa-prerender) with [npm](https://npmjs.org):

```sh
$ npm install bot-koa-prerender`
```

### Usage

```js
var prerender = require('bot-koa-prerender');

// Options
var options = {
  prerender: PRERENDER_SERVER_URL   // optional, default:'http://service.prerender.io/'
  protocol: 'http',                 // optional, default: this.protocol
  host: 'www.risingstack.com',      // optional, default: this.host,
  prerender_token: ''               // optional or process.env.PRERENDER_TOKEN
};

// Use as middleware
app.use(prerender(options));
```

## Heavily inspired by

Gergely Nemeth <mail@nemethgergely.com> (http://twitter.com/nthgergo)

## License

MIT
