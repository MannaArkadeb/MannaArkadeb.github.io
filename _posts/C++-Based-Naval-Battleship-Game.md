---
title: "Naval Battleship Game in C++"
date: 2026-05-20
author: "Arkadeb Manna"
words_per_minute: 50
read_time: true
tags:
  - C++
  - Multithreading
  - Socket Programming
  - Object Oriented Programming
---

## Project Overview
* This project is a complete Battleship game implemented entirely in C++.
* It utilizes a Linux/WSL client-server architecture built in distinct functional layers.
* Multiple players can connect to the server via sockets, wait in a synchronized matchmaking queue, and play turn-based matches directly from the terminal.

## Introduction
* The project is a networked adaptation of the classic Battleship board game.
* Upon joining a match, each player is assigned a hidden 10x10 grid where their fleet of ships is placed automatically.
* Players take turns attacking specific board coordinates until only one player remains alive.
* The server acts as the central orchestrator, independently managing client connections, matchmaking queues, turn order, and game state validation.
* The client executable is strictly a thin layer responsible only for handling user input and printing server messages to the terminal.

## Key Features
* **Object-Oriented Design**: Utilizes robust classes to encapsulate the game model; for instance, `Ship.h` represents a ship object, `Board.h` represents the grid, and `MatchSession.h` encapsulates an entire active match.
* **Socket Programming**: Facilitates TCP server/client communication using POSIX sockets and a custom text-based network messaging protocol.
* **Multithreading**: The server leverages `std::thread` to run three distinct thread types: an accept thread to queue incoming TCP clients, a match thread to group players, and dedicated worker threads that run concurrently for every active game.
* **Synchronization**: Employs `std::mutex` and `std::condition_variable` to safely synchronize data and handle the matchmaking queue.
* **Dynamic Multiplayer Support**: Supports standard 1v1 play (using coordinates like `A5`) as well as matches with three or more players using the extended `ATTACK <target> <coord>` format.
* **Clean Architecture**: Achieves strict modular separation between the networking protocol, the server logic, the client interface, and the core game model.

## Conclusion
* This application successfully demonstrates the development of a fully functional, networked game from scratch in C++.
* It highlights practical implementations of advanced system concepts, including concurrent multithreading, thread synchronization, and OS-level socket communication.
* Through its modular file organization and layered design, the project serves as a highly structured and easily maintainable codebase.