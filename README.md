# Mock for the redis-py client library

![Build Status](https://travis-ci.org/avto-dev/mockredis.svg?branch=master)
![License](https://img.shields.io/github/license/avto-dev/mockredis?longCache=true)

Supports writing tests for code using the [redis-py][redis-py] library
without requiring a [redis-server][redis] install.

## Installation

Use pip:

```bash
$ pip install mockredispy
```

## Usage

Both `mockredis.mock_redis_client` and `mockredis.mock_strict_redis_client` can be
used to patch instances of the *redis client*.

For example, using the [mock][mock] library:

    @patch('redis.Redis', mock_redis_client)

Or:

    @patch('redis.StrictRedis', mock_strict_redis_client)

## Testing

Many unit tests exist to verify correctness of mock functionality. In addition, most
unit tests support testing against an actual redis-server instance to verify the tests
against ground truth. See `mockredis.tests.fixtures` for more details and disclaimers.

## Supported python versions

 - Python 2.7
 - Python 3.2
 - Python 3.3
 - Python 3.4
 - PyPy
 - PyPy3

## Attribution

This code is shamelessly derived from work by [John DeRosa][john].

 [redis-py]: https://github.com/andymccurdy/redis-py
 [redis]:    http://redis.io
 [john]:     http://seeknuance.com/2012/02/18/replacing-redis-with-a-python-mock/
 [mock]:     http://www.voidspace.org.uk/python/mock/
