# PlaywrightWithTS

PlaywrightWithTS is a simple starter project for end-to-end (E2E) testing using Playwright and TypeScript.

## Features

- Tests written in TypeScript using Playwright test runner
- Cross-browser testing (Chromium, Firefox, WebKit)
- Easy setup and commands to run tests locally or in CI

## Prerequisites

- Node.js (LTS, e.g. >= 16)
- npm or yarn

## Install

1. Clone the repository:

   git clone https://github.com/Nishants79/PlaywrightWithTS.git
   cd PlaywrightWithTS

2. Install dependencies:

   npm install
   # or
   yarn install

3. Install Playwright browsers (required to run tests):

   npx playwright install

## Run tests

- Run the full test suite (headless):

  npx playwright test

- Run a single test file:

  npx playwright test path/to/test.spec.ts

- Run tests headed (useful for debugging):

  npx playwright test --headed

- Open Playwright test runner UI for debugging a specific file:

  npx playwright test --debug

## Configuration

This project uses `playwright.config.ts` to configure projects, timeouts, reporters, and browsers. Adjust that file to change test behavior or browser targets.

## Project structure

- tests/            — test files (TypeScript)
- playwright.config.ts — Playwright configuration
- package.json      — scripts and dependencies

(If your project uses different paths or filenames, update this section accordingly.)

## Scripts (example)

Add helpful scripts to package.json if not present, for example:

```json
{
  "scripts": {
    "test": "playwright test",
    "test:headed": "playwright test --headed",
    "test:report": "playwright show-report"
  }
}
```

## CI

In CI, install dependencies and Playwright browsers before running tests. Example steps:

- npm ci
- npx playwright install --with-deps
- npx playwright test

## Contributing

Contributions are welcome. Typical workflow:

1. Fork the repo
2. Create a feature branch
3. Add tests and/or code
4. Open a pull request describing your changes

Please include tests for any new features and ensure all tests pass locally.

## Troubleshooting

- If tests fail due to missing browsers, run `npx playwright install`.
- For flaky tests, try `--retries 2` or run in headed mode to inspect failures.

## Notes

Update this README to reflect any repository-specific scripts, folders, or settings.
