Create a diagram depicting the situation where the user creates a new note using the single-page version of the app.
```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server->>browser: STATUS 201 created
    deactivate server
    Note right of browser: Uses the JavaScript code it fetched from the server for form data.