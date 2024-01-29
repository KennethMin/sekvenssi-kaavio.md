```mermaid
sequenceDiagram
    participant selain
    participant palvelin

    selain->>palvelin: Käyttäjä painaa tallenna nappia
    activate selain
    selain->>palvelin: POST https://studies.cs.helsinki.fi/exampleapp/newnote
palvelin->>selain: GET https://studies.cs.helsinki.fi/exampleapp/notes
palvelin->>selain: GET main.js
palvelin->>selain: GET main.css
palvelin->>selain: GET data.json

    palvelin-->>selain: { "content": "Uusi muistiinpano", "date": "2024-1-29" }
    deactivate selain

    Note right of selain: Selain päivittää käyttöliittymän näyttämään uuden muistiinpanon
