# GitHub Repositories Fetcher (Sprint 03)

A responsive and interactive web application built using **HTML5, CSS3, and Vanilla JavaScript (ES6+)** that retrieves public GitHub repositories through the GitHub REST API. The application provides secure input validation, asynchronous API communication, repository sorting, CSV export, offline detection, and accessible user feedback while maintaining a clean, framework-free architecture.

This project was developed as part of **Sprint 03** to demonstrate practical knowledge of asynchronous JavaScript, REST API integration, dynamic DOM manipulation, client-side validation, error handling, accessibility, and responsive web development.

---

## Live Demo

**Live Deployment:** *Add Deployment URL Here*

---

## Features

### Core Features

* Search public repositories by GitHub username.
* Retrieve all repositories using the GitHub REST API.
* Automatic pagination support for users with more than 100 repositories.
* Display repository name, description, language, stars, forks, and last updated date.
* Open GitHub profile directly from search results.
* Open individual repositories in new browser tabs.
* Responsive repository card layout for mobile, tablet, and desktop devices.

---

## Search & Sorting

* Validate GitHub usernames before making API requests.
* Sort repositories by:

  * Last Updated
  * Star Count
  * Repository Name
* Cached search results prevent unnecessary API requests for repeated searches.
* Display repository count after every successful search.

---

## Network & User Experience

* Detect browser online and offline status.
* Display connection status banner automatically.
* Retry failed requests with a dedicated Retry button.
* Loading spinner while repositories are being retrieved.
* Empty state when users have no public repositories.
* Accessible error messages for invalid usernames and failed requests.

---

## CSV Export

* Export repository information to CSV.
* Includes repository metadata:

  * GitHub Username
  * GitHub Profile
  * Export Date
  * Total Repository Count
* Properly escapes special characters and quotation marks.
* UTF-8 BOM support for Excel compatibility.

---

## Security

* Username validation using regular expressions.
* Uses `textContent` and DOM APIs instead of unsafe `innerHTML`.
* URL parameters are safely encoded using `encodeURIComponent()`.
* Fetch requests automatically timeout using `AbortController`.

---

## Technical Highlights

### REST API Integration

The application communicates with the GitHub REST API using the Fetch API and asynchronous JavaScript. It supports automatic pagination to retrieve complete repository collections.

### Dynamic DOM Rendering

Repository cards are created entirely through JavaScript using DOM methods, ensuring secure rendering without HTML injection.

### Error Handling

Comprehensive client-side error handling manages:

* Invalid usernames
* User not found (404)
* API rate limiting (403)
* Network failures
* Request timeout
* Server-side errors (5xx)

### Accessibility

The application includes:

* Semantic HTML5 structure
* ARIA labels
* Screen-reader-only labels
* Keyboard focus management
* Live regions for status updates

### Modern JavaScript

The project demonstrates:

* ES6 Modules (Object Pattern)
* Async/Await
* Promises
* Fetch API
* AbortController
* Arrow Functions
* Template Literals
* Destructuring
* Array Methods

---

## Technologies Used

* HTML5
* CSS3
* CSS Variables
* Responsive CSS Grid
* Flexbox
* Vanilla JavaScript (ES6+)
* Fetch API
* GitHub REST API
* AbortController
* CSV File Generation

---

## Testing

### Search Testing

* Search valid GitHub usernames.
* Validate invalid username formats.
* Verify "User not found" handling.

### API Testing

* Retrieve repositories successfully.
* Test pagination with users having more than 100 repositories.
* Simulate API rate limiting.

### Network Testing

* Simulate offline mode.
* Verify offline notification banner.
* Test Retry functionality after reconnecting.

### Sorting Testing

* Sort repositories by stars.
* Sort repositories alphabetically.
* Sort repositories by last updated date.

### Export Testing

* Export repository list as CSV.
* Verify metadata rows.
* Open CSV in Excel or Google Sheets.

---

## Project Structure

```text
project/
│
├── index.html
├── style.css
├── script.js
├── README.md
└── assets/
```

---

## Conclusion

This project demonstrates practical frontend development using native web technologies while integrating an external REST API. It combines asynchronous programming, responsive design, client-side validation, accessibility, dynamic DOM rendering, secure data handling, network awareness, and CSV export into a maintainable and framework-independent application.
