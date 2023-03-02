```mermaid

sequenceDiagram
  participant browser
  participant server

  browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server -->> browser: HTML document
  deactivate server

  browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server -->> browser: CSS stylesheet
  deactivate server   

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js   
  activate server
  server-->>browser: JS
  deactivate server
  
  note over browser: JS sends GET request for data
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server-->>browser: JSON data
  deactivate server
  note over browser: Data rendered to page
 ```
