# Tech News Aggregator (Dart)

A small Dart workspace that pulls trending stories from the Hacker News API, auto-categorizes them by topic, and lets you browse, filter, and export them from an interactive command-line app — with colorized terminal output.

## Packages

This is a multi-package Dart workspace with three local packages:

| Package | Description |
|---|---|
| [`tech_news_api`](./tech_news_api) | API client for fetching and categorizing stories from the [Hacker News API](https://github.com/HackerNews/API). Handles retries, timeouts, and JSON parsing. |
| [`tech_news_cli`](./tech_news_cli) | The interactive command-line application — the main entry point for the project. |
| [`terminal_colors`](./terminal_colors) | A tiny, dependency-free extension on `String` for ANSI terminal styling (headers, warnings, errors, success messages). |

## Features

- **Fetch top stories** from Hacker News with a configurable count
- **Auto-categorization** of stories into topics via keyword matching:
  - AI & Machine Learning
  - Programming & Dev
  - Security & Privacy
  - DevOps & Systems
  - Startups & Tech Business
  - General Tech
- **Filter** previously fetched stories by category or keyword
- **Export** results to a Markdown digest file
- **Resilient networking**: automatic retries with backoff and request timeouts
- **Colorized CLI output** for headers, warnings, errors, and success messages

## Getting Started

### Prerequisites

- [Dart SDK](https://dart.dev/get-dart) `^3.0.0`

### Install dependencies

```bash
cd tech_news_cli
dart pub get
```

### Run the CLI

```bash
dart run bin/main.dart
```

### Commands

Once running, use these commands at the `[news-aggregator] >` prompt:

```
top <COUNT>       - Fetch top news (default: 10)
filter <CATEGORY> - Filter fetched stories (e.g., filter AI)
export <FILE>     - Save last fetched news to file (e.g., export news.md)
exit              - Quit application
```

### Example session

```
[news-aggregator] > top 5

Fetching top 5 tech headlines...

--------------------------------------------------
1. [AI & Machine Learning] New open-weight model released
   Points: 342 | Comments: 128 | By: someuser
   URL: https://example.com/article

[news-aggregator] > filter AI
[news-aggregator] > export digest.md
Saved 5 stories to digest.md
```

## Project Structure

```
tech_news_workspace/
├── tech_news_api/       # HTTP client + models + categorization logic
│   └── lib/src/
│       ├── client.dart  # TechNewsApiClient (fetch + retry logic)
│       └── models.dart  # NewsStory model + categorizeStory()
├── tech_news_cli/       # CLI entry point
│   └── bin/main.dart
└── terminal_colors/     # ANSI color styling extension on String
    └── lib/src/terminal_colors_base.dart
```

## Running Tests

From each package directory:

```bash
dart test
```

## License

Add a license of your choice (e.g. MIT) before publishing.
