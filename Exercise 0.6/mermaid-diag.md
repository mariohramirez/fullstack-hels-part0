# Exercise 0.5: Single page app diagram

Diagram depicting the situation where the user goes to SPA version of the notes app

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User fills the form and the click the save button

    Note right of browser: The event handler in the javascript file adds the note to the list and rerender the note list on the page

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: Status 201 {"message":"note created"}
    deactivate server

```
