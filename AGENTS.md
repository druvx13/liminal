# Agent Instructions for Liminal Space Prompt Crafter

Welcome, AI Agent! This document provides guidance for working on the Liminal Space Prompt Crafter project.

## Project Overview

This is a client-side web application built with HTML, Tailwind CSS (via CDN), and vanilla JavaScript (ES Modules). It helps users craft prompts for generating liminal space images using the Google Gemini API.

## Key Files

*   `index.html`: The main entry point and structure of the application.
*   `src/js/main.js`: Contains all JavaScript logic, including UI interactions, API calls to Gemini, and state management.
*   `src/css/style.css`: For any custom CSS rules not covered by Tailwind CSS utilities.
*   `README.md`: Project documentation. Please keep this updated with any significant changes.

## Development Guidelines

1.  **JavaScript:**
    *   All new JavaScript code should be written using ES Module patterns.
    *   Place all JavaScript code within the `src/js/` directory. `main.js` is the primary script.
    *   Ensure DOM manipulations are efficient and event listeners are managed correctly (e.g., added on `DOMContentLoaded` and removed if elements are dynamically destroyed, though current app structure is simple).
    *   API interactions with Google Gemini are handled in `main.js`. Be mindful of API key handling (currently uses `localStorage` after a user prompt).

2.  **CSS Styling:**
    *   Primarily use [Tailwind CSS](https://tailwindcss.com/) utility classes for styling directly in `index.html`.
    *   The Tailwind configuration is currently embedded in a `<script>` tag in `index.html`.
    *   If custom, more complex CSS is absolutely necessary, add it to `src/css/style.css` and ensure it's well-commented.

3.  **HTML Structure:**
    *   Maintain semantic HTML where possible.
    *   All user-facing content is within `index.html`.

4.  **API Key Handling:**
    *   The Google Gemini API key is essential. The application currently prompts the user for their key and stores it in `localStorage`.
    *   **Do not hardcode API keys into the source code.**
    *   Error handling for API key issues (invalid key, quota exceeded, etc.) should be user-friendly.

5.  **Dependencies:**
    *   External libraries (React, ReactDOM, GoogleGenAI) are loaded via CDN using `importmap` in `index.html`. Avoid adding new CDN dependencies unless strictly necessary and discussed.
    *   Tailwind CSS and Google Fonts are also loaded via CDN.

6.  **Code Quality & Readability:**
    *   Write clear, commented code, especially for complex logic.
    *   Ensure functions and variables have descriptive names.
    *   Format your code consistently.

7.  **Testing:**
    *   Thoroughly test all changes in a browser.
    *   Verify core functionalities: manual prompt building, AI assistant, image generation (requires a valid API key), history persistence, and UI responsiveness.
    *   Check the browser console for errors.

8.  **Commits and Pull Requests:**
    *   Write clear and concise commit messages.
    *   If submitting a pull request, provide a detailed description of the changes and the reasoning behind them.

## Updating Documentation

*   If you make changes that affect the project's features, setup, or architecture, please update `README.md` accordingly.
*   If you modify how agents should interact with the codebase, update this `AGENTS.md` file.

Thank you for your contribution!
