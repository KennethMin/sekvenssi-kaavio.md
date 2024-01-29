```mermaid
sequenceDiagram
    participant selain
    participant palvelin

    selain->>palvelin: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate selain
    palvelin-->>selain: HTML document
selain->>palvelin: GET https://studies.cs.helsinki.fi/exampleapp/main.css
palvelin-->>selain: main.css
selain->>palvelin: GET https://studies.cs.helsinki.fi/exampleapp/main.js
palvelin-->>selain: GET main.js
selain->>palvelin: GET https://studies.cs.helsinki.fi/exampleapp/data.json
palvelin-->>selain: [{ "conent": "Hello", "date": "2024-29-1"}]

    deactivate selain

    Note right of selain: Selain hakee muistiinpanot jonka jälkeen päivittää ne näkyville
