sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: HTTP 201 Created
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code. A new note is created, added to the note list with the notes.push(note) command, re-renders the note list on the page, and sends the new note to the server. 