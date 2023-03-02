```mermaid
sequenceDiagram;
  participant browser
  participant server
  
  note over browser: Note Saved
  note over browser: Create note object from form
  note over browser: Push object to notes array
  note over browser: Render notes array 
  note right of browser: Send note object as JSON to server

  browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
  activate server
  server -->> browser: 201 created
  deactivate server
  ```
