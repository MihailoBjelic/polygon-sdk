# Minimal

[![CircleCI](https://circleci.com/gh/0xPolygon/minimal.svg?style=svg)](https://circleci.com/gh/0xPolygon/minimal)
[![Join the chat at https://gitter.im/0xPolygon/minimal](https://badges.gitter.im/0xPolygon/minimal.svg)](https://gitter.im/0xPolygon/minimal?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Modular implementation of different stacks of the Ethereum blockchain.

This is a work in progress so architectural changes are expected in the near future. Besides, there exist intentional panics intended to cover areas where the logic is unfinished or the test coverage is not complete.

## Commands

### Agent

Starts the Ethereum client for the mainnet:

```
$ go run main.go agent [--config ./config.json]
```

The configuration file can be specified either in HCL or JSON format:

```
{
    "data-dir": "/tmp/data-dir"
}
```

Some attributes can be also set from the command line:

```
$ go run main.go agent --config ./config.json --data-dir /tmp/local --port 30304 --log-level TRACE
```

The values from the CLI have preference over the ones in the configuration file.

### Dev

Start a development chain with instant sealing:

```
$ go run main.go dev
```

### Genesis

Generates a test genesis file:

```
$ go run main.go genesis
```
