sequenceDiagram
  participant Browser as Browser
  participant Server as Server

  Browser ->> Server: "GET" https://studies.cs.helsinki.fi/exampleapp/notes
  Server -->> Browser: HTML Document (Web Page)
  Note right of Browser: There is an input field with "save" button to add notes.
  Note right of Browser: Once the web page appears, the browser requests for the JS file
  Browser ->> Server: "GET" https://studies.cs.helsinki.fi/exampleapp/main.js
  Server -->> Browser: Javascript File
  Note right of Browser: After receiving the JS file. It executes the code in it and fetches the JSON from server
  Browser ->> Server: "GET" https://studies.cs.helsinki.fi/exampleapp/data.json
  Server -->> Browser: JSON Content
  Note right of Browser: Now you can see some notes on the screen from the server.
  Note right of Browser: Lets add a new note. Type some text into the input field and click "save"
  Browser ->> Server: "POST" https://studies.cs.helsinki.fi/exampleapp/new_note
  Note right of Browser: This sends the text to the location "notes" on the server
  Note left of Server: creates a new json.object in the server with the text
  Note right of Browser: Browser Refreshes
  Browser ->> Server: "GET" https://studies.cs.helsinki.fi/exampleapp/data.json
  Server -->> Browser: JSON Content (Updated JSON)
  Note right of Browser: New Note Appears in the notes
