# Pretty UTC

A simple, user-friendly web tool to convert UTC timestamps to your local time. Instantly parse ISO 8601 and SQL-style UTC times, see the result in your time zone, and get a human-friendly "relative time" (e.g., "2 hours ago").

## Features

- **UTC to Local Time Conversion**: Enter a UTC timestamp and instantly see its value in your local time zone.
- **Supports Common Formats**: Accepts ISO 8601 and SQL timestamp formats (e.g. `2025-12-01 10:32:22.750456+00`).
- **Auto-Detection**: Automatically detects your system time zone.
- **Relative Time**: See how far in the past or future the input timestamp is from now (e.g., "in 5 minutes", "3 hours ago").
- **Use Current Time**: Quickly fill in the current UTC time with a single click.
- **Clipboard Paste**: Paste a UTC timestamp from your clipboard.
- **Helpful Errors**: Graceful error messages for invalid inputs.

## How It Works

1. **Enter a UTC timestamp** (e.g. `2025-12-01 10:32:22.750456+00`) or use the "Use Current Time" button.
2. Click **Convert** (or paste from clipboard).
3. Results include:
   - Your local time zone name
   - The converted local date & time (with seconds, 12-hour clock)
   - The date in a readable form
   - How long ago (or into the future) the time is, compared to now
   - The parsed UTC date for reference

## Example

```
UTC Timestamp:    2025-12-01 10:32:22.750456+00

Local Time:       3:32:22 PM
Date:             December 1, 2025
Time Zone:        Asia/Kolkata
Relative Time:    in 3 hours

Original Parse:   Mon, 01 Dec 2025 10:32:22 GMT
```

## Usage

Just [open `index.html`](index.html) in your browser.  
*No installation or backend setup required!*

## Tech Stack

- **Vanilla JavaScript**
- [Tailwind CSS](https://tailwindcss.com/) for styles
- [Font Awesome](https://fontawesome.com/) for icons
- Responsive & mobile-friendly

## Code Overview

- All logic and UI in a single file: [`index.html`](index.html)
- Main functions:
  - `processTime()`: Parses and validates timestamps; updates the result fields.
  - `setNow()`: Sets the field to the current UTC time.
  - `pasteFromClipboard()`: Pastes timestamp from clipboard and attempts conversion.
  - `getRelativeTime()`: Formats time difference as natural language ("in 3 hours").

## Accepted Formats

- `YYYY-MM-DD HH:MM:SS+00`
- `YYYY-MM-DDTHH:MM:SSZ`
- Supports input with milliseconds/microseconds.

## License

MIT

---

Made for developers, DBAs, testers, and anyone needing a quick time conversion from UTC!
