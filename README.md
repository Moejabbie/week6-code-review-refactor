# Week 6 Assignment: Code Review Refactor

## Project Description

This project refactors a messy JavaScript click analytics dashboard. The original program used multiple loose global variables to store application data.

I refactored the code by combining the variables into one centralized `appState` object. I also created a `renderApp()` function to synchronize the application state with the webpage.

## Refactoring

The original variables were:

* currentCount
* totalClicksEver
* whatWasTheLastAction
* trackingHistoryLogArray

These variables were combined into one `appState` object.

The application now follows this process:

**User Action → Update appState → renderApp() → Update the DOM**

## How to Run

1. Download or clone this repository.
2. Open `refactor-challenge.html` in a web browser.
3. Click the Increment and Decrement buttons.
4. Verify that the count, total clicks, last action, and activity log update correctly.

## Testing

The application was tested by:

* Clicking Increment twice.
* Confirming the count becomes 2.
* Confirming total clicks becomes 2.
* Confirming the last action displays Incremented.
* Clicking Decrement once.
* Confirming the count becomes 1.
* Confirming total clicks becomes 3.
* Confirming the last action displays Decremented.
* Checking the browser Console for runtime errors.

## AI Assistance

I used an AI assistant as a Senior Software Engineer/code reviewer to help identify the problems with the original global-variable structure and recommend a centralized `appState` object.

### AI Prompt Used

"Act as a Senior Software Engineer conducting a code review. I have inherited a messy JavaScript script that tracks dashboard clicks using loose global variables. Please refactor this data footprint into a single, clean JavaScript object called appState. Provide the code structure and explain why bundling loose variables into a unified state object makes application data easier to manage, protect, and track as programs expand. Keep the feedback beginner-friendly and do not rewrite the event listeners yet."

## Technologies

* HTML
* CSS
* JavaScript
* GitHub
* GitHub Pages
* AI-assisted code review
