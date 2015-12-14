# feathers-errors

[![Build Status](https://travis-ci.org/feathersjs/feathers-errors.png?branch=master)](https://travis-ci.org/feathersjs/feathers-errors)

> Common error types for feathers apps

## Getting Started

Feathers errors come with feathers by default. So typically you don't need to install it at all.

## Documentation

#### Current Error Types:

* `BadRequest`: 400
* `NotAuthenticated`: 401
* `PaymentError`: 402
* `Forbidden`: 403
* `NotFound`: 404
* `MethodNotAllowed`: 405
* `NotAcceptable`: 406
* `Timeout`: 408
* `Conflict`: 409
* `Unprocessable`: 422
* `GeneralError`: 500
* `NotImplemented`: 501
* `Unavailable`: 503

**Pro Tip:** Feathers service adapters (ie. mongodb, memory, etc.) already emit the appropriate errors for you. :-)

#### Usage:

```js
import errors from 'feathers-errors';

// If you were to create an error yourself.
var notFound = new errors.NotFound('User does not exist'));

// You can wrap existing errors
var existing = new errors.GeneralError(new Error('I exist'));

// You can also pass additional data
var data = new errors.BadRequest('Invalid email', {email: 'sergey@google.com'});
```

## Release History
__1.0.1__
- Fixing critical bug [#15](https://github.com/feathersjs/feathers-errors/issues/15)

__1.0.0__
 - converting to ES6
 - making structure consistent with other plugins
 - removing error handlers [#11](https://github.com/feathersjs/feathers-errors/issues/11)

__0.2.0__

- Adding support for mongoose errors [Issue #5](https://github.com/feathersjs/feathers-errors/issues/5).

__0.1.4__

- Adding more error types
- Changing `missing` to `fourOhFour`
- Making library feathers core compatible

__0.1.3__

- Adding a default error page

__0.1.2__

- Minor bug fixes

__0.1.1__

- Exposing error types directly via `var types = require('feathers-errors').types;`

__0.1.0__

- Initial release

## License

Copyright (c) 2015 Feathers Contributors

Licensed under the [MIT license](LICENSE).
