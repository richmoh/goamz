# GoAMZ

[![Sourcegraph](https://sourcegraph.com/github.com/richmoh/goamz/-/badge.svg)](https://sourcegraph.com/github.com/richmoh/goamz?badge)

[![Build Status](https://travis-ci.org/richmoh/goamz.png?branch=master)](https://travis-ci.org/richmoh/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/richmoh/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/richmoh/goamz/aws
github.com/richmoh/goamz/cloudwatch
github.com/richmoh/goamz/dynamodb
github.com/richmoh/goamz/ec2
github.com/richmoh/goamz/elb
github.com/richmoh/goamz/iam
github.com/richmoh/goamz/kinesis
github.com/richmoh/goamz/s3
github.com/richmoh/goamz/sqs
github.com/richmoh/goamz/sns

github.com/richmoh/goamz/exp/mturk
github.com/richmoh/goamz/exp/sdb
github.com/richmoh/goamz/exp/ses
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/richmoh/goamz](http://godoc.org/github.com/richmoh/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/richmoh/goamz/ec2`
* `$ go get github.com/richmoh/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get launchpad.net/gocheck`

Then run go test as usual:

`$ go test github.com/richmoh/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

`$ gotest -i`
