# Streams

[![Go Report Card](https://goreportcard.com/badge/github.com/msales/streams)](https://goreportcard.com/report/github.com/msales/streams)
[![Build Status](https://travis-ci.org/msales/streams.svg?branch=master)](https://travis-ci.org/msales/streams)
[![Coverage Status](https://coveralls.io/repos/github/msales/streams/badge.svg?branch=master)](https://coveralls.io/github/msales/streams?branch=master)
[![GitHub release](https://img.shields.io/github/release/msales/streams.svg)](https://github.com/msales/streams/releases)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/msales/streams/master/LICENSE)

Streams is a light weight, simple stream processing library. While Kafka is the main use case for Streams, it is
flexible enough to be used for any form of processing from any source.

**Note:** This is currently a work in progress. 

## Installation

You can install streams using `go get`

```shell
go get github.com/msales/streams
```

## Concepts

Streams breaks processing into two basic parts.

* **Sources** reads and handles position from a data source.

* **Processor** processes the data, optionally passing it on or marking the sources position. A sink is just a processor
  the does not forward the data on.
  
* **Context** gives processors an abstract view of the current state.