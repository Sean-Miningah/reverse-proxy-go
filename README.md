# Reverse Proxy Server in Golang 

This repository contains a simple implementation of a reverse proxy server in Golang. The proxy server is configured using a YAML file, it can route different backend servers based on the specified endpoints. 

## Table of Contents 

- [Introduction](#introduction)
- [Usage](#usage)
- [Configuration](#configuration)
- [Run the Proxy Server](#run-the-proxy-server)

## Introduction 
The proxy server is implemented using Golang and leverages the `net/http` package. It provides a flexible way to route incoming requests to differenet backend servers based on the configurations specified in a YAML file.

## Usage 
To use the reverse proxy server, follow the steps outlined below: 

1. Clone the repository to your local machine.
2. Configure the proxy server using the `config.yaml` file.
3. Run the proxy server using the provided Golang code.

## Configuration 
The configuration file (`config.yaml`) is used to define the server settings and resources (backend servers) to which requests should be proxied. Below is an example configuration: 

```yaml
server: 
  host: "localhost:
  listen_port: "8080"

resources: 
  - name: Server1 
    endpoint: /server1 
    destination_url: "http://localhost:9001"
  - name: Server2 
    endpoint: /server2 
    destination_url: "http://localhost:9002"
  - name: Server3
    enpoint: /server3 
    destination_url: "http://localhost:9003"
```

## Run the Proxy Server
To run the proxy server, execute the go run command 

```bash
go run main.go
```