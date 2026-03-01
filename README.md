# T20 World Cup (Team Selection)

## Problem Statement

The agenda is to find the best combination of players possible in order to generate most runs with batsmen as well as have a solid no. of bowlers in order to weaken the opposite team.

## Objective

- The team should be able to score at least 180 runs on an average
- They should be to defend 150 runs on an average

<i>“WE DON’T KNOW THE STRENGTHS AND WEAKNESSES OF OUR OPPONENTS BUT GIVE ME THE BEST 11 FROM THE GIVEN DATA”</i>


## Architecture

```mermaid
graph TD
    classDef process fill:#bbf,stroke:#333,stroke-width:2px;
    classDef storage fill:#bfb,stroke:#333,stroke-width:2px;
    classDef bi fill:#fbb,stroke:#333,stroke-width:2px;

    A[Web Scraping Scripts <br/> Bright Data / JS]:::process -->|Extract| B[(Raw Data<br/>JSON Files)]:::storage
    B -->|Load| C[Data Preprocessing <br/> Jupyter Notebook / Pandas]:::process
    C -->|Transform| D[(Processed Data<br/>CSV Files)]:::storage
    D -->|Import| E[Power BI <br/> Data Modeling & Dashboards]:::bi
```

## Tech Stack

* **Web Scraping:** Bright Data (JavaScript)
* **Data Preprocessing:** Python(Pandas)
* **Data Visualization & Modeling:** Microsoft Power BI