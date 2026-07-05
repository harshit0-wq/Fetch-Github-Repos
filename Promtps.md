# AI Prompt Engineering & Development Log

This document records the major prompts, implementation decisions, and architectural improvements made during the development of the **GitHub Repositories Fetcher (Sprint 03).**

---

# Prompt 01 – Project Planning & API Architecture

## Objective

* Understand Sprint 03 requirements.
* Design a responsive GitHub repository search interface.
* Integrate the GitHub REST API.
* Plan modular application architecture.
* Handle asynchronous data retrieval.

## Outcome

* Built a modular application using separate Validation, API, Export, UI, and App modules.
* Established asynchronous repository retrieval using the Fetch API.
* Added automatic pagination support for users with large repository collections.

---

# Prompt 02 – Dynamic Rendering & Secure DOM Manipulation

## Objective

* Dynamically generate repository cards.
* Prevent Cross-Site Scripting (XSS).
* Build reusable rendering methods.
* Maintain responsive layouts.

## Outcome

* Rendered repository cards using DOM APIs.
* Used `textContent` for secure content insertion.
* Implemented responsive repository grids using CSS Grid and Flexbox.
* Generated accessible repository links and metadata.

---

# Prompt 03 – Validation, Search & Sorting

## Objective

* Validate GitHub usernames.
* Retrieve repositories from the GitHub API.
* Support repository sorting.
* Display meaningful feedback for empty searches.

## Outcome

* Implemented regular expression username validation.
* Retrieved repositories asynchronously.
* Added sorting by updated date, star count, and repository name.
* Displayed repository counts and empty-state messages.

---

# Prompt 04 – Error Handling & User Experience

## Objective

* Handle API failures gracefully.
* Detect network interruptions.
* Provide loading indicators.
* Improve accessibility.

## Outcome

* Added loading spinner during API requests.
* Implemented online/offline detection.
* Displayed retry options for recoverable failures.
* Added accessible status messages and keyboard focus management.

---

# Prompt 05 – CSV Export & Performance Improvements

## Objective

* Export repository information as CSV.
* Cache repeated searches.
* Improve application responsiveness.
* Record user interactions.

## Outcome

* Generated downloadable CSV reports with repository metadata.
* Cached previous search results to reduce unnecessary API calls.
* Used AbortController to prevent long-running requests.
* Logged important user interactions for debugging and analytics.

---

# Summary

The application evolved through multiple development iterations focused on asynchronous programming, REST API integration, responsive interface design, secure DOM manipulation, accessibility, comprehensive error handling, client-side performance optimization, and CSV export.

The final solution is a responsive Vanilla JavaScript application that demonstrates modern frontend engineering practices using native browser APIs while maintaining a clean, modular, secure, and framework-independent architecture.
