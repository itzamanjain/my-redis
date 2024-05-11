---
Title: Custom Redis Server
---

This is a simple implementation of a Redis-like server written in JavaScript using Node.js.

## Overview

This custom Redis server aims to mimic a subset of the functionality provided by Redis, a popular in-memory data structure store. It listens for TCP connections on a specified port and handles basic Redis commands such as `SET` and `GET`. The server maintains an in-memory key-value store to store data.

## Features

- **SET command**: Stores a key-value pair in the server's memory.
- **GET command**: Retrieves the value associated with a given key from the server's memory.
- **Error handling**: Basic error handling for invalid commands and missing keys.

## Usage

1. **Installation**:
   - Ensure you have Node.js installed on your system.
   - Clone this repository to your local machine.

2. **Running the server**:
   - Navigate to the project directory in your terminal.
   - Run `npm install` to install dependencies.
   - Start the server by running `node server.js`.

3. **Connecting to the server**:
   - The server listens for connections on port 8000 by default. You can adjust the port as needed.
   - Use a Redis client or Telnet to connect to the server on the specified port (`telnet localhost 8000`).

4. **Sending commands**:
   - Once connected, you can send Redis-like commands to the server.
   - Supported commands:
     - `SET key value`: Sets the value of the specified key.
     - `GET key`: Retrieves the value associated with the specified key.

## Example

```sh
telnet localhost 8000
SET mykey hello
GET mykey
