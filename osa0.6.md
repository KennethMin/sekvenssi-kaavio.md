```mermaid
sequenceDiagram
    participant selain
    participant palvelin

    selain->>palvelin: Käyttäjä luo uuden muistiinpanon
selain->>palvelin: POST https://studies.cs.helsinki.fi/exampleapp/newnote
    activate selain
    palvelin-->>selain: JSON-File mikä sisältää muistiinpanon


    deactivate selain

    Note right of selain: Selain päivittää sivun dynaamisesti lisäämällä muistiinpanon ilman että sivu ladataan uudestaan.
