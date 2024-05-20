```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>server: Process the new note 
    server-->>browser: Respond with success status and the new note
    deactivate server
    browser-->>browser: Update the UI with new note
