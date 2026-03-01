# T20 World Cup (Team Selection)

## Problem Statement

The agenda is to find the best combination of players possible in order to generate most runs with batsmen as well as have a solid no. of bowlers in order to weaken the opposite team.

## Objective

- The team should be able to score at least 180 runs on an average
- They should be to defend 150 runs on an average

<i>“WE DON’T KNOW THE STRENGTHS AND WEAKNESSES OF OUR OPPONENTS BUT GIVE ME THE BEST 11 FROM THE GIVEN DATA”</i>


## Architecture

%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ffffff', 'primaryTextColor': '#333333', 'primaryBorderColor': '#0052cc', 'lineColor': '#0052cc', 'tertiaryColor': '#ebecf0'}}}%%
graph LR
    subgraph Ingestion["1. Data Ingestion 🌐"]
        A[<b>Bright Data / JS</b><br/>Web Scraping Scripts]:::process
    end

    subgraph Storage1["Raw Storage 🗄️"]
        B[(<b>JSON Files</b><br/>Raw Data)]:::storage
    end

    subgraph Processing["2. Data Processing ⚙️"]
        C[<b>Jupyter Notebook</b><br/>Python / Pandas]:::process
    end

    subgraph Storage2["Processed Storage 🗃️"]
        D[(<b>CSV Files</b><br/>Clean Data)]:::storage
    end

    subgraph BI["3. Business Intelligence 📊"]
        E[<b>Power BI</b><br/>Data Modeling & Dashboards]:::bi
    end

    A -->|Extract| B
    B -->|Load| C
    C -->|Transform| D
    D -->|Import| E

    classDef process fill:#e1f5fe,stroke:#0288d1,stroke-width:2px,color:#01579b,rx:10px,ry:10px;
    classDef storage fill:#e8f5e9,stroke:#388e3c,stroke-width:2px,color:#1b5e20,rx:5px,ry:5px;
    classDef bi fill:#fff3e0,stroke:#f57c00,stroke-width:2px,color:#e65100,rx:10px,ry:10px;


## Tech Stack

* **Web Scraping:** Bright Data (JavaScript)
* **Data Preprocessing:** Python(Pandas)
* **Data Visualization & Modeling:** Microsoft Power BI