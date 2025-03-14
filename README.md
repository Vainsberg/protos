# SSO Protobuf Definitions

This repository contains Protocol Buffer definitions for the SSO (Single Sign-On) service.

## Structure

- `proto/sso/` - Contains the protobuf definition files
- `gen/go/sso/` - Contains the generated Go code

## Services

### Auth Service

The Auth service provides the following RPCs:
- `Register` - Register a new user
- `Login` - Login user and get auth token
- `IsAdmin` - Check if user has admin privileges

## Usage

### Prerequisites

- Protocol Buffers compiler (protoc)
- Go plugins for Protocol Buffers

### Generating Code

To regenerate the Go code from .proto files:

```bash
protoc --proto_path=. \
  --go_out=gen/go \
  --go_opt=paths=source_relative \
  --go-grpc_out=gen/go \
  --go-grpc_opt=paths=source_relative \
  proto/sso/sso.proto
``` 