# SimpleRPCService

## Description
SimpleRPCService is a Python-based RPC application using `rpyc`. The server exposes functions for arithmetic operations, text manipulation, system info retrieval, and list sorting. Clients connect to the server, invoke exposed functions remotely, and receive results in real-time using a threaded server.

## Architecture
- **RPC Server**: Hosts multiple exposed functions using `rpyc.Service` and handles multiple clients via `ThreadedServer`.
- **RPC Client**: Connects to the server, invokes exposed functions, and receives results in real-time.

## Exposed Functions
1. `add_numbers(a, b)` - Returns the sum of two numbers.
2. `subtract_numbers(x, y)` - Returns the difference between two numbers.
3. `reverse_text(text)` - Returns the reversed string.
4. `get_system_info()` - Returns a dictionary with system info (`system` and `version`).
5. `sort_list(numbers)` - Returns a sorted list of numbers.

## Technologies Used
- Python
- `rpyc` library
- Threaded RPC server

## How to Run
1. Install `rpyc` if not already installed:
```bash
pip install rpyc
python server.py
python client.py
The server can handle multiple clients concurrently using ThreadedServer.

This project demonstrates remote procedure calls and client-server communication in Python.

Designed for educational purposes to illustrate RPC concepts and Python networking.
