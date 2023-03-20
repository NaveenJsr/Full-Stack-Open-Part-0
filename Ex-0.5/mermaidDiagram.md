sequenceDiagram
  participant User
  participant WebBrowser
  participant Server

  User->>WebBrowser: Enters https://studies.cs.helsinki.fi/exampleapp
  WebBrowser->>Server: Requests /exampleapp
  Server-->>WebBrowser: Returns index.html
  WebBrowser->>Server: Requests /exampleapp/main.css
  Server-->>WebBrowser: Returns main.css
  WebBrowser->>Server: Requests /exampleapp/main.js
  Server-->>WebBrowser: Returns main.js
  WebBrowser->>Server: Requests /exampleapp/data.json
  Server-->>WebBrowser: Returns data.json
  WebBrowser->>Server: Requests /exampleapp/spa
  Server-->>WebBrowser: Returns index.html for single-page app
  WebBrowser->>Server: Requests /exampleapp/spa/main.js
  Server-->>WebBrowser: Returns main.js for single-page app
  WebBrowser->>Server: Requests /exampleapp/spa/data.json
  Server-->>WebBrowser: Returns data.json for single-page app
