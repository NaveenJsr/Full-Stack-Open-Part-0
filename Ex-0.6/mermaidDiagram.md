sequenceDiagram
  participant User
  participant WebBrowser
  participant Server
  participant Database

  User->>WebBrowser: Enters https://studies.cs.helsinki.fi/exampleapp/spa
  WebBrowser->>Server: Requests single-page app files
  Server-->>WebBrowser: Returns single-page app files
  User->>WebBrowser: Clicks "New note"
  WebBrowser->>Server: Sends request to create new note
  Server->>Database: Sends request to save new note
  Database-->>Server: Returns confirmation of saved note
  Server-->>WebBrowser: Returns confirmation of saved note
  WebBrowser->>Server: Requests updated note list
  Server->>Database: Sends request for updated note list
  Database-->>Server: Returns updated note list
  Server-->>WebBrowser: Returns updated note list
