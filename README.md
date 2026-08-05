# Phone_Book_Directory

A simple desktop contact management application built in Java using Swing. It lets you add, view, search, and delete contacts through a clean graphical interface, with all data saved to a local file so nothing is lost between sessions.

## Overview

This was built as a mini project for the Object Oriented Programming Lab (CS2002-1) at NMAM Institute of Technology, under the Department of Artificial Intelligence and Machine Learning Engineering.

**Submitted by:**
- Deepali Sherigar
- AIML Department
- NMAM Institute of Technology

## Features

- **Add Contact** — Enter a name and phone number through simple input dialogs
- **View Contacts** — See the full list of saved contacts at a glance
- **Search Contact** — Case-insensitive lookup by name
- **Delete Contact** — Remove a contact by name, with a friendly message if it isn't found
- **Save Contacts** — Persist all contacts to a text file (`contacts.txt`) so data survives across sessions

## How It Works

- **`Contact`** — A simple model class holding a name and phone number.
- **`ContactBook`** — Manages the collection of contacts (backed by an `ArrayList`) and provides methods to add, search, delete, save, and load contacts.
- **`MiniPro`** — The main class that builds the Swing GUI, wires up button click listeners, and connects user actions to the `ContactBook` logic.

Contacts are stored as comma-separated `name,phone` lines in `contacts.txt`, which is read on startup (if it exists) and written whenever you hit **Save Contacts**.

## Tech Stack

- Java (core language)
- Java Swing (`javax.swing`) — GUI components and dialogs
- Java AWT Event handling (`java.awt.event`) — button click listeners
- Java I/O (`java.io`) — file reading/writing for persistence
- `java.util.ArrayList` and `Iterator` — in-memory contact storage and safe removal

## Getting Started

### Prerequisites
- Java Development Kit (JDK) installed

### Compile and Run

```bash
javac MiniPro.java
java MiniPro
```

On launch, the app will attempt to load any existing contacts from `contacts.txt` in the same directory. If the file doesn't exist yet, it simply starts with an empty contact list.

## Usage

1. Click **Add Contact** and enter a name and phone number when prompted.
2. Click **View Contacts** to see all saved contacts in a message dialog.
3. Click **Search Contact** and type a name (case doesn't matter) to find a specific entry.
4. Click **Delete Contact** and type a name to remove that contact.
5. Click **Save Contacts** to write the current contact list to `contacts.txt`.

## Error Handling

- Deleting a non-existent contact shows a "Contact not found!" message instead of crashing.
- File read/write issues are caught and reported through dialog boxes rather than terminating the app.
- Loading gracefully skips the load step if `contacts.txt` doesn't exist yet.

## Future Enhancements

- Add fields like email or address to the `Contact` class
- Replace positional (null) layout with a responsive layout manager
- Add contact editing functionality
- Switch from plain text storage to a more structured format (e.g., CSV with headers, or a small database)

## References

1. [GeeksforGeeks — Java Programming Language Tutorial](https://www.geeksforgeeks.org/java/)
2. [JavaFX Documentation](https://openjfx.io/)
3. [W3Schools — Java Servlets Tutorial](https://www.w3schools.com/java/java_servlets.asp/)
