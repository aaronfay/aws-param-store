[![Build Status](https://travis-ci.org/vandium-io/aws-param-store.svg?branch=master)](https://travis-ci.org/vandium-io/aws-param-store)
[![npm version](https://badge.fury.io/js/aws-param-store.svg)](https://badge.fury.io/js/aws-param-store)

# aws-param-store

Module for loading parameter-store values from AWS SSM

## Features
* Loads parameters by path
* Recursively loads and decoded parameters by default
* Paginates results automatically
* Supports synchronous querying of parameters
* Promise based
* Can run inside AWS Lambda environment
* AWS Lambda Node.js 6.10.x compatible


## Installation
Install via npm.

	npm install aws-param-store --save

## Getting Started

```js
const awsParamStore = require( 'aws-param-store' );

awsParamStore.newQuery( '/project1/service1/production' )
    .execute()
    .then( (parameters) => {

        // set env vars from here
    });
```

## Feedback

We'd love to get feedback on how to make this tool better. Feel free to contact us at `feedback@vandium.io`

## License

[BSD-3-Clause](https://en.wikipedia.org/wiki/BSD_licenses)