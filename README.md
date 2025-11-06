# GoIT Python Core - Home Work 07: Final CLI Assistant Integration

## Project Overview

This repository implements the final version of the **Console Assistant Bot**, merging **Object-Oriented Programming (OOP)** models with a robust **CLI interface**. The solution demonstrates advanced use of **decorators**, **exception handling**, and **datetime** logic.

***

## Repository Structure and Functionality (Solutions)

| File | Function / Component | Description of Functionality |
| :--- | :--- | :--- |
| **Classes** | `Field`, `Phone`, `Birthday`, `Record`, `AddressBook` | Implements the core OOP data structure with **validation** (10 digits, DD.MM.YYYY format) and **inheritance**. |
| **`AddressBook`** | `get_upcoming_birthdays()` | **Advanced Date Logic:** Calculates birthdays in the next 7 days, including automatic **weekend shift** (Saturday/Sunday → Monday). |
| **Handlers** | `@input_error` | **Universal Decorator:** Protects all command handlers against `ValueError`, `KeyError`, and `IndexError`, ensuring the bot remains stable. |
| **CLI Commands** | `add-birthday`, `show-birthday`, `birthdays` | Integrates new commands for managing and viewing birthday data within the `AddressBook` structure. |

***

## Execution Instructions and Commands

| Command | Usage Example | Functionality |
| :--- | :--- | :--- |
| **`add [Name] [Phone]`** | `add John 1234567890` | Adds a new contact or phone number. |
| **`change [Name] [Old] [New]`** | `change John 1234 9999` | Finds and edits an existing phone number. |
| **`add-birthday [Name] [Date]`** | `add-birthday John 25.12.1990` | Adds the contact's date of birth (validated). |
| **`birthdays`** | `birthdays` | Displays all contacts to be congratulated in the next week, adjusted for weekends. |
| **`close` / `exit`** | `exit` | Terminates the application. |