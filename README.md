# Edge Protocol Translator Examples

This repository contains the Protocol Translator examples for the Edge.

## pt-example

Pt-example is a basic example of the C-API and pt-client usage.

## mqttpt-example

`mqttpt-example` is an example of a protocol translator that connects to endpoints using MQTT. It can be used
without real MQTT hardware using provided Mosquitto MQTT simulator scripts. The endpoints may
publish for example temperature and humidity values to Device Management.

## blept-example

The `blept-example` is a protocol translator reference implementation for use with Bluetooth Low Energy (BLE) devices that implement a Bluetooth Low Energy Generic Attributes (GATT) server. It connects to BLE devices and translates their GATT services and characteristics into Open Mobile Alliance (OMA) Lightweight Machine to Machine (LwM2M) Objects and Resources.

## simple-js-examples

The `simple-js-examples` are different from the rest of the examples. Instead of using the provided `pt-client`
library these examples use Edge Core protocol translator and management API directly.

These are examples on how a protocol translator or management API application can be created using Javascript.
See the [simple-js-examples/README.md](simple-js-examples/README.md) for instructions.

# Building the examples

This section describes how the build the examples using Ubuntu 16.04.

## Dependencies

Following dependencies are needed in the build system.

* librt
* libstdc++
* OPTIONAL for mqttpt-example: libmosquitto

Install these:

```
$ apt install build-essential git libc6-dev
$ apt install libmosquitto-dev mosquitto-clients
$ apt install libglib2.0-dev
```
## Preparing all the sources

Please run the following to clone and update all the git modules.
```
$ git submodule update --init --recursive
```

## Building

Makefile has options to build any of the pt-examples separately, or all at the same.

To make all examples without debug information and with default trace level, run
```
$ make build-all-examples
```
It will build the examples to `build/bin` directory.

To make all examples with debug information and debug trace level, run
```
$ make build-all-examples-debug
```

It will build the examples to `build-debug/bin` directory.

To make all examples with ThreadSanitizer and debug trace level, run
```
$ make build-all-examples-sanitize
```

It will build the examples to `build-sanitize/bin` directory.

Running `make all` will generate `build`, `build-debug` and `build-sanitize` directories.

Please note following:
mqttpt-example will not be built if the libmosquitto is not installed.

For more examples, see the rules in the Makefile.

# Running the examples

Each of the examples has a README.md file that documents how to run the example.
