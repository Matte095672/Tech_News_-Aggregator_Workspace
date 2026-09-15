# Tech News Aggregator Workspace

A Dart-based command-line application that retrieves, processes, and displays technology news from external news APIs.

## Project Description

The **Tech News Aggregator** is a command-line application developed using Dart. It connects to a news API to retrieve technology-related news articles and presents the information through a simple command-line interface.

The project demonstrates API integration, JSON data processing, object-oriented programming, command-line interaction, error handling, logging, terminal styling, and automated testing.

## Objectives

The project aims to:

1. Retrieve technology news from a news API.
2. Process and convert JSON responses into Dart objects.
3. Provide a command-line interface for searching and viewing technology news.
4. Implement error handling for network and API-related problems.
5. Use terminal colors to improve the command-line interface.
6. Implement logging for application activities and errors.
7. Organize the application using a Dart workspace with multiple packages.
8. Implement automated tests for the project components.

## Features

* Search and retrieve technology news through an external API.
* Display news titles, descriptions, sources, and publication information.
* Support command-line interaction.
* Handle API and network errors.
* Use terminal colors for improved output.
* Record application events and errors through logging.
* Convert API JSON data into Dart models.
* Include automated tests.
* Organize functionality into reusable Dart packages.

## Technologies Used

* **Dart**
* **News API**
* **HTTP**
* **JSON**
* **Dart Testing Framework**
* **ANSI Terminal Colors**
* **Git**
* **GitHub**

## Project Structure

```text
TECH_NEWS_AGGREGATOR_WORKSPACE/
│
├── terminal_colors/
│   ├── lib/
│   │   ├── src/
│   │   │   ├── ansi.dart
│   │   │   └── terminal_colors_base.dart
│   │   ├── terminal_colors.dart
│   │   └── ...
│   ├── test/
│   └── pubspec.yaml
│
├── news_api/
│   ├── lib/
│   │   ├── src/
│   │   │   ├── client.dart
│   │   │   ├── exceptions.dart
│   │   │   ├── models.dart
│   │   │   └── news_api_base.dart
│   │   ├── news_api.dart
│   │   └── ...
│   ├── test/
│   ├── example/
│   └── pubspec.yaml
│
├── news_cli/
│   ├── bin/
│   │   ├── main.dart
│   │   └── news_cli.dart
│   ├── lib/
│   │   ├── src/
│   │   │   ├── alert_command.dart
│   │   │   ├── command_base.dart
│   │   │   ├── help_command.dart
│   │   │   ├── logging_config.dart
│   │   │   └── query_command.dart
│   │   └── news_cli.dart
│   ├── test/
│   └── pubspec.yaml
│
├── pubspec.yaml
├── pubspec.lock
└── .gitignore
```

## Package Description

### terminal_colors

The `terminal_colors` package provides reusable terminal styling and ANSI color constants for the command-line interface.

It improves the readability and presentation of news information displayed in the terminal.

### news_api

The `news_api` package handles communication with the external technology news API.

It contains the news data models, API client, JSON processing, and exception handling required to retrieve and process news articles.

### news_cli

The `news_cli` package provides the command-line interface of the application.

It handles user commands, technology news queries, help commands, alerts, logging, and formatted terminal output.

## Requirements

Before running the project, make sure the following are installed:

* Dart SDK 3.8.1 or later
* Git
* Internet connection
* Access to the configured news API

## Installation

Clone the repository:

```bash
git clone https://github.com/lacsoncherryrose-byte/TECH_NEWS_AGGREGATOR_WORKSPACE.git
```

Navigate to the project directory:

```bash
cd TECH_NEWS_AGGREGATOR_WORKSPACE
```

Get the project dependencies:

```bash
dart pub get
```

## How to Run

Navigate to the CLI package:

```bash
cd news_cli
```

Run the application:

```bash
dart run
```

## Example Usage

The application can be used to search and retrieve technology news through the command-line interface.

Example command:

```text
news > query technology
```

Example output:

```text
[INFO] Initiating technology news query: technology

Title: New Technology Innovations and Trends
Source: Technology News
Published: 2026-09-14

Description: Latest developments and updates in the technology industry.
```

The displayed news information is retrieved from the configured news API.

## API

This project uses an external **Technology News API** to retrieve news articles.

The API response may contain information such as:

* Article ID
* Article title
* Description
* News source
* Author
* Publication date
* Article URL
* Image URL

The application processes the JSON response and converts the relevant information into Dart objects before displaying it in the command-line interface.

## Error Handling

The application implements error handling for possible problems such as:

* Network connection failures
* API request failures
* Invalid API responses
* Invalid news data
* Missing article information
* Timeout errors
* Invalid command-line arguments

Exceptions are handled using Dart exception-handling mechanisms to prevent unexpected application crashes and provide useful error messages to the user.

## Logging

The CLI package includes logging functionality for recording application events and errors.

Logging helps identify problems during application execution and makes troubleshooting easier.

Examples of logged events include:

* API connection attempts
* News search requests
* Successful API responses
* Network errors
* Invalid requests
* Application exceptions

## Testing

The project contains automated tests for the application components.

To run the tests, use:

```bash
dart test
```

The tests verify important functionality of the API, data models, command-line components, error handling, and other project packages.

## Screenshots

Screenshots of the application can be added to this section to demonstrate the actual output and functionality.

### Technology News Query

Add a screenshot of the technology news query command here.

### News Results

Add a screenshot showing the technology news information returned by the application.

### Test Results

Add a screenshot showing the successful test execution.

## GitHub Repository

The source code and project documentation are available in this repository:

**TECH NEWS AGGREGATOR WORKSPACE**

https://github.com/lacsoncherryrose-byte/TECH_NEWS_AGGREGATOR_WORKSPACE

## Developer

**Diza D. Matte**

BSIT 3
Palawan State University – Taytay Campus

## Course

**IT7/L – System Integration and Architecture 1**

## Conclusion

The **Tech News Aggregator** demonstrates how Dart can be used to build a modular command-line application that communicates with an external API to retrieve and process technology news.

The project applies important software development concepts including API integration, JSON processing, data modeling, object-oriented programming, command-line interaction, error handling, logging, terminal styling, automated testing, and GitHub-based project management.

Through its modular workspace structure, the project also demonstrates how multiple Dart packages can work together to create a maintainable and reusable application.
