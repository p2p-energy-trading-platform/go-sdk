# GridX Go SDK

Generated Go protobuf and gRPC SDK for the GridX - P2P Energy Trading Platform.

This SDK contains Go protobuf message types and Go gRPC stubs generated from the [`protobuf`](https://github.com/p2p-energy-trading-platform/protobuf) repository.

## Purpose

The Go SDK is used by Go microservices for:

- Kafka message encoding/decoding
- gRPC inter-service communication

## Generated Files

Do not manually edit files inside:

```text
gen/
```

These files are generated automatically from the protobuf contract repo.

## Install

```bash
go get github.com/p2p-energy-trading-platform/go-sdk@v0.2.0
```

## Usage

```go
package main

import (
	testv1 "github.com/p2p-energy-trading-platform/go-sdk/gen/gridx/test/v1"
)

func main() {
	money := &testv1.TestMoney{
		CurrencyCode: "LKR",
		Units:        100,
		Nanos:        0,
	}

	_ = money
}
```

## Versioning

This SDK follows the same version as the protobuf contract release.

Example:

```text
protobuf v0.2.0
go-sdk   v0.2.0
```