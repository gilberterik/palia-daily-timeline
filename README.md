# Ring Clock

A simple, single-file web application that displays a clock with a unique ring-style face. The clock shows both the user's local time (IRL) and a corresponding in-game time, based on a 60:1 time ratio (60 real minutes = 24 game hours).

## Purpose

This project was created to provide a visual representation of time that maps a full 24-hour cycle onto a single 60-minute rotation. The primary use case is for games or other applications where time moves faster than in the real world. The clock face is designed to be clean and intuitive, with a single hand that completes a full rotation every hour.

## Setup

To run the application, simply open the `index.html` file in a web browser. No server or special setup is required. For development, you can use a simple local server to avoid any potential issues with `file://` protocols:

```bash
python -m http.server 8000
```

Then, navigate to `http://localhost:8000/index.html` in your browser.

## Usage

The clock displays two times:

*   **In-Game Time**: The inner ring of the clock face represents a 24-hour day. The hand's position indicates the current in-game time.
*   **IRL Time**: The user's local time is displayed below the clock face for reference.

The hand of the clock syncs to the top of each real-world hour. This means that at the beginning of every hour (e.g., 1:00, 2:00, etc.), the hand will be at the 12 o'clock position.

## Project Structure

The project consists of a single HTML file, `index.html`, which contains all the necessary HTML, CSS, and JavaScript. The only external dependency is a background image, which is located in the `bg/` directory.

*   `index.html`: The main application file.
*   `bg/`: Contains the background image for the clock face.
*   `AGENTS.md`: Provides guidelines for agents working on the repository.
