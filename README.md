# Liminal Space Prompt Crafter

## Introduction

The Liminal Space Prompt Crafter is a web-based application designed to help users create detailed and evocative prompts for generating AI images of liminal spaces. It leverages the power of the Google Gemini API to assist in prompt generation and to create the final images. Users can layer concepts manually or use an AI assistant to transform simple ideas into rich prompts.

## Features

*   **Manual Prompt Construction:** Select from curated lists of:
    *   Spatial Archetypes (e.g., "Empty Corridor," "Airport at Night")
    *   Atmospheric Modifiers (e.g., "Golden Hour Haze," "Flickering Fluorescents")
    *   Temporal/Emotional Amplifiers (e.g., "1990s Nostalgia," "Uncanny Familiarity")
*   **Surprise Me:** Randomly selects one option from each category to quickly generate a base prompt.
*   **AI Prompt Assistant:** Input a simple idea (e.g., "a forgotten mall"), and the Gemini API will generate a detailed liminal space prompt.
*   **Image Generation:**
    *   Utilizes the Gemini API (Imagen model) to generate images based on the crafted prompt.
    *   Editable final prompt area.
    *   Option to add a negative prompt to exclude unwanted elements.
    *   Selectable aspect ratios for the generated image (16:9, 9:16, 4:3, 3:4, 1:1).
*   **Generation History:**
    *   Automatically saves generated images, their prompts, and negative prompts to the browser's local storage.
    *   View and manage your past creations.
    *   Quickly reuse or delete history items.
*   **Copy to Clipboard:** Easily copy the final prompt.
*   **Download Image:** Download the generated image directly.

## Tech Stack

*   **HTML:** Structure of the web page.
*   **Tailwind CSS:** Utility-first CSS framework for styling. (Loaded via CDN)
*   **JavaScript (ES Modules):** Application logic, DOM manipulation, and API interactions.
*   **Google Gemini API:**
    *   `gemini-2.5-flash` for AI-assisted prompt crafting.
    *   `imagen-3.0-generate-002` for image generation.
*   **Google Fonts (Inter):** For typography. (Loaded via CDN)

## Setup and Usage

This is a client-side application and can be run by simply opening the `index.html` file in a modern web browser that supports ES Modules.

**API Key Configuration:**

The application requires a Google Gemini API key to function correctly (for AI Prompt Assistant and Image Generation features).

1.  **Obtain an API Key:** If you don't have one, you'll need to get a Google Gemini API key from the [Google AI Studio](https://aistudio.google.com/app/apikey).
2.  **Using the Key:**
    *   When you first try to use a feature that requires the API (like "Ask Assistant" or "Generate Image"), the application will prompt you to enter your API key.
    *   Enter your key in the browser prompt. The key will be stored in your browser's `localStorage` for future sessions on the same browser.
    *   If the key is invalid or there's an API issue, an error message will be displayed, and the stored key might be cleared. You'll be prompted again on the next attempt.

**Security Note:** The API key is stored in your browser's local storage. While this is convenient for a client-side application, **never commit your API key directly into the source code or share an `index.html` file with your key embedded if you are hosting it publicly.** For personal local use, the prompt mechanism is generally acceptable. For wider distribution or a more secure setup, a backend proxy to handle API requests would be recommended.

## File Structure

```
.
├── LICENSE
├── README.md
├── AGENTS.md         # Instructions for AI agents (to be created)
├── index.html        # Main HTML file
├── assets/           # For static assets (currently unused, icons are inline SVG)
└── src/
    ├── css/
    │   └── style.css     # Custom CSS (if any)
    └── js/
        └── main.js       # Main JavaScript application logic
```

## Contributing

Contributions are welcome! If you have suggestions or improvements:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes.
4.  Test thoroughly.
5.  Submit a pull request with a clear description of your changes.

## License

This project is licensed under the terms of the `LICENSE` file (currently Apache 2.0).
