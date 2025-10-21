# Mermaid eksempler
For å rendre disse i VS Code, må du installere en utvidelse for Mermaid. Jeg bruker [denne](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid).

Noen av disse eksemplene rendrer ikke riktig i GitHub, men de gjør det i VS Code med utvidelsen installert.

## Enkelt flytdiagram
``` mermaid
flowchart TD
    A-->B
    A-->C
    B-->D
    C-->D
    D-->E
```

## Enkelt flytdiagram, håndtegnet stil
``` mermaid
---
config:
  look: handDrawn
---
flowchart TD
    A-->B
    A-->C
    B-->D
    C-->D
    D-->E
```

## Flytdiagram med mange forbindelser

``` mermaid
flowchart LR
    A-->B
    A-->C
    B-->D
    C-->D
    D-->E
    E-->A
    D-->C
    D-->B
    E-->B
    A-->E
    B-->A
    B-->E
```

## Flytdiagram med farger og former og slikt

``` mermaid
flowchart TD
    A(Jul) -->|Få penger| B(Dra og handle)
    style A fill:red,stroke:black,stroke-width:4px,shadow:shadow
    B --> C{La meg tenke}
    style B fill:green,stroke:black,stroke-width:4px,shadow:shadow
    C -->|En| D[Laptop]
    style C fill:blue,stroke:black,stroke-width:4px,shadow:shadow
    C -->|To| E[iPhone]
    C -->|Tre| F[fa:fa-car Bil]
    style D fill:yellow,stroke:black,stroke-width:2px,shadow:shadow
    style E fill:brown,stroke:black,stroke-width:2px,shadow:shadow
    style F fill:navy,stroke:black,stroke-width:2px,shadow:shadow
```

## Flytdiagram med mange alternativer og ryddig arrangert kode

``` mermaid
flowchart LR
    id1(Boks med rund kant)
    id2([Stadion])
    id3[(Database)]
    id4((Sirkel))
    id5{{Heks}}
    id6[\Parallellogram\]
    id7[\Trapesoid/]

    id1-- 1. linje ---id2
    id1--> |2. linje| id3
    id1--- |3. linje| id4
    id2-.-|4. linje| id5
    subgraph En boks rundt greier
    id3 == 5. linje ==> id6
    end
    subgraph En annen boks rundt greier
    id4 <--> id7 --> id6
    end

    style id1 fill:green,stroke:black
    style id2 fill:white,stroke:#f66,stroke-dasharray: 5, 5
    style id3 fill:#66f,stroke:#f6f,stroke-width:4px
    style id4 fill:red,stroke:yellow
    style id5 fill:orange,stroke:white
    style id6 fill:yellow,stroke:blue
    style id7 fill:brown,stroke:blue
```

# Enkelt gantt

``` mermaid
gantt
    title Et Gantt Diagram

    Fullført oppgave          :done,    task, 2024-01-06,2024-01-08
    Aktiv oppgave             :active,  task2, 2024-01-09, 3d
    Fremtidig oppgave         :         task3, after task2, 5d
    Fremtidig oppgave2        :         task4, after task3, 5d
```

## Gantt med flere alternativer

``` mermaid
gantt
    title Et Gantt Diagram
    dateFormat  YYYY-MM-DD
    excludes weekends
    
    section Demo Seksjon
    Første oppgave  : done,a1, 2023-12-24, 9d
    Andre oppgave : active,a2, 2024-01-01, 14d
    Milepæl   : milestone, m1, after a2, 0d
    Kritisk oppgave   : crit,a3, 2024-01-10, 9d
    Siste oppgave   : a4,after a2, 8d
    Prosjektslutt : milestone, m2, 2024-02-02, 0d

    section Hjelp kanalen
    Lik      :active,a5,2024-01-5  , 2d
    Kommenter : a6,after a5, 7d
    Abonner   : crit,a7,after a6,8d

```

## Kakediagram

``` mermaid
pie showData
    title PetterTechs innhold
    "Windows 365" : 13
    "Azure" : 28
    "PowerShell" : 3
```

## Sankey diagram
``` mermaid
sankey
Arbeidsuke,Skriving,14
Arbeidsuke,Tegning,10
Arbeidsuke,Moter,16
```

## Enkelt gitGraph diagram

``` mermaid
gitGraph:
    commit id: "Første commit"
    commit id: "Gjorde ting"
    
    branch branchingOff
    
    checkout branchingOff
    commit id: "Gjorde noen branch-greier"
    commit id: "Gjorde mer branch-greier"
    checkout main
    commit id: "Gjorde noen flere ting"
    merge branchingOff id: "Fletter tilbake"

    commit id: "Post-fletting greier"
    commit id: "Ferdig?"
```
## Tankekart

``` mermaid
mindmap
  root((Hjernen min))
    ))Dungeons & Dragons((
      {{En kampanje}}
        ((DM oppgaver))
          Aethenia
            Kongeriker
            Byer
            Landsbyer
            NPCer
            Guder
          Forberede
          Kjøre
          Følge opp
          Hjelpe spillere
      {{En annen kampanje}}
        ((Halldur
        Trubadur))
          Bard
          Dvergearv
          Støtte
          Trylleformler
          Linene
    ))YouTube((
      {{Følge opp}}
        Kommentarer
        Forslag
      {{Lage innhold}}
        )Azure(
          EPAC
          Arc
          AVD
          Dev Box
          Spot VMer
        Kode greier
          Powershell
          Bicep
          Mermaid
          IaC
        )Windows 365(
            Start
            Bruk
            Funksjoner
            Nyheter
```

## Tidslinje

``` mermaid
%%{init: { 'logLevel': 'debug', 'theme': 'base' } }%%
timeline
    title PetterTech YouTube kanal
    2015: Opprettelse av kanal
    2021: Februar <br> Første video postet : Juni <br> Rebranding til PetterTech : Oktober <br> Første video til å nå 1000 visninger
    2022: August <br> Nådde totalt 25 opplastinger : September <br> Første video til å nå 10k visninger
    2023: Oktober <br> Nådde 1000 abonnenter <br> : November <br> Kvalifisert for YouTube partnerskap
```

## Reise

``` mermaid
    journey
        title En PetterTech dag
        section Morgen
            Våkne: 1
            Spise frokost: 5
            Gå tur med hunden: 6
            Gå på jobb på hjemmekontor: 8
        section Arbeidsdag
            Jobb: 8
            Lunsj: 9
            Jobb: 7
            Avslutt jobb: 9
        section Kvelder
            Middag: 8
            Greier med barna: 8
            Gå tur med hunden: 8
            Sove: 8
```

## Sekvensdiagram

``` mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hei John, hvordan går det?
    loop Helsesjekk
        John->>John: Kjempe mot hypokondrisme
    end
    Note right of John: Rasjonelle tanker <br/>seirer...
    John-->>Alice: Strålende!
    John->>Bob: Hva med deg?
    Bob-->>John: Kjempebra!
```

## Kvadrantdiagram

``` mermaid
quadrantChart
    x-axis x1 --> x2
    y-axis y1 --> y2
    quadrant-1 Kommenter
    quadrant-2 Lik
    quadrant-3 Abonner
    quadrant-4 Del
```

## Kvadrantdiagram med prikker

``` mermaid
quadrantChart
    x-axis x1 --> x2
    y-axis y1 --> y2
    quadrant-1 Kommenter
    quadrant-2 Lik
    quadrant-3 Abonner
    quadrant-4 Del
    dot1: [0.3, 0.7]
    dot2: [0.6, 0.2]
    dot3: [0.8, 0.9]
    dot4: [0.2, 0.4]
    dot5: [0.6, 0.7]
```

## Kvadrantdiagram med prikker, farger og slikt

``` mermaid
%%{init: {"quadrantChart": {"chartWidth": 500, "chartHeight": 500}, "themeVariables": {"quadrant1Fill": "#5abf5f","quadrant2Fill": "#24bda8","quadrant3Fill": "red","quadrant4Fill": "#bd5e24","quadrantTitleFill": "green", "quadrantPointFill": "black", "quadrantPointTextFill": "black", "quadrant1TextFill": "white", "quadrant2TextFill": "white", "quadrant3TextFill": "white", "quadrant4TextFill": "white"} }}%%
quadrantChart
    title Kvadrantdiagram
    x-axis forst pa x --> andre pa x
    y-axis forst pa y --> andre pa y
    quadrant-1 Ovre hoyre
    quadrant-2 Ovre venstre
    quadrant-3 Nedre venstre
    quadrant-4 Nedre hoyre
    Dot1: [0.3, 0.7]
    Dot2: [0.6, 0.2]
    Dot3: [0.8, 0.9]
    Dot4: [0.2, 0.4]
    Dot5: [0.5, 0.1]
    Dot6: [0.1, 0.3]
```


## Klassediagram

``` mermaid
classDiagram
class Dyr {
        +navn: string
        +alder: int
        +lagLyd(): void
    }

    class Hund {
        +rase: string
        +bjeff(): void
    }

    class Katt {
        +farge: string
        +mjau(): void
    }

    Dyr <|-- Hund
    Dyr <|-- Katt
```

## Relasjonsdiagram

``` mermaid
erDiagram
    KUNDE }|..|{ LEVERINGSADRESSE : har
    KUNDE ||--o{ ORDRE : plasserer
    KUNDE ||--o{ FAKTURA : "ansvarlig for"
    LEVERINGSADRESSE ||--o{ ORDRE : mottar
    FAKTURA ||--|{ ORDRE : dekker
    ORDRE ||--|{ ORDREVARE : inkluderer
    PRODUKTKATEGORI ||--|{ PRODUKT : inneholder
    PRODUKT ||--o{ ORDREVARE : "bestilt i"
```

## Tilstandsdiagrammer


``` mermaid
stateDiagram-v2
    [*] --> Stille
    Stille --> [*]
    Stille --> Beveger
    Beveger --> Stille
    Beveger --> Krasj
    Krasj --> [*]
```

``` mermaid
stateDiagram-v2
    [*] --> Aktiv

    state Aktiv {
        [*] --> NumLockAv
        NumLockAv --> NumLockPå : EvNumLockTrykket
        NumLockPå --> NumLockAv : EvNumLockTrykket
        --
        [*] --> CapsLockAv
        CapsLockAv --> CapsLockPå : EvCapsLockTrykket
        CapsLockPå --> CapsLockAv : EvCapsLockTrykket
        --
        [*] --> ScrollLockAv
        ScrollLockAv --> ScrollLockPå : EvCapsLockTrykket
        ScrollLockPå --> ScrollLockAv : EvCapsLockTrykket
    }
```

## Arkitekturdiagram

``` mermaid
architecture-beta
    group azure(cloud)[Azure]

    service db(database)[MySQL] in azure
    service disk1(disk)[Lagringskonto A] in azure
    service disk2(disk)[Lagringskonto B] in azure
    service server(server)[VM] in azure

    db:L -- R:server
    disk1:T -- B:server
    disk2:T -- B:db
```