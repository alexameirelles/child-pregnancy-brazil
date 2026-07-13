# Births to Girls Aged 14 and Younger in Brazil

URL: 

*A data-driven investigation into births among girls aged 14 and younger
in Brazil between 2004 and 2024.*

> Project 2 for the Lede Program in Data Journalism at Columbia University.

------------------------------------------------------------------------

# Overview

This project investigates births to girls aged 14 and younger in Brazil between 2004 and 2024.

Although Brazilian law guarantees access to abortion when a pregnancy results from rape (and any sexual act involving a child under 14 is legally classified as rape), more than 12,000 babies were born to girls in this age group in 2024 alone.

Using more than twenty years of microdata from Brazil's Live Birth Information System (SINASC), the project explores how these births evolved over time, where they are concentrated, and the demographic profile of the girls who gave birth.

Unlike my previous project, where I used D3.js primarily for a line chart and bar charts, this project was designed as an opportunity to further develop my data visualization skills using "vanilla" D3. 

Rather than focusing on a novel analytical approach, I intentionally chose a relatively straightforward analysis so I could devote more time to designing and implementing different types of interactive visualizations. The project combines a line chart, a choropleth map, a grid of small multiple line charts, and waffle charts, all built with D3.js.

This project is intentionally data-driven. While the analysis reveals a deeply troubling reality, I believe the story would be stronger with interviews featuring girls, families, healthcare professionals, and child rights experts to provide context beyond the numbers. Due to the limited timeframe, this first version focuses exclusively on the data analysis.

For the visual design—particularly the color palette—I drew inspiration from *A Journey Through Infertility*, an interactive story by *The Pudding*: https://pudding.cool/2026/03/ivf/

------------------------------------------------------------------------

# Data

The analysis is based on microdata from SINASC (Sistema de Informações
sobre Nascidos Vivos), accessed through Base dos Dados: https://basedosdados.org/dataset/48ccef51-8207-40ee-af5b-134c8ac3fb8c?table=80359f9a-8189-4693-bdf7-ebf7be0d2fff 

Base dos Dados is a nonprofit, open-source organization working to make high-quality public data universally accessible. It does this by developing innovative tools, producing and sharing knowledge, and promoting a culture of transparency and open data.

Using Python and the basedosdados package, I executed two SQL queries against the Base dos Dados repository:

- One to retrieve individual-level records for births to girls aged 14 and younger (2004–2024);

- Another to retrieve the total number of live births by municipality and year, used to calculate rates per 1,000 live births.

Additional datasets include:

- IBGE state boundaries (GeoJSON)

------------------------------------------------------------------------

# Methodology

## 1. Data collection

Data were queried directly from Base dos Dados using SQL inside Python
notebooks.

Categorical variables such as race/color, marital status and education
were translated using the official SINASC dictionaries, while
municipality and state codes were matched to their corresponding names.

The processed datasets were exported as CSV files for analysis.

## 2. Data analysis

The analysis was conducted in Python using pandas. Since the data were accessed through Base dos Dados, they were already standardized, documented, and well structured, requiring virtually no cleaning before analysis. 

Instead, the work focused on exploratory data analysis and the calculation of demographic, geographic, and temporal indicators. 

A broad set of variables, including age, race/color, marital status, education, geographic distribution, and birth trends, was examined. However, the final story highlights only those that best supported the project's central findings.

Visualizations were built using D3.js, including an animated line chart,
choropleth map, sparklines and waffle charts.

------------------------------------------------------------------------

# Main findings

- Births to girls aged 14 and younger have declined substantially since 2004.
- In 2024, 12,007 babies were born to girls in this age group.
- Northern states consistently recorded the highest rates per 1,000 live births.
- Nearly three-quarters of the girls who gave birth were registered as parda or black.
- One in ten were recorded as married or living in a stable union.


------------------------------------------------------------------------

# Skills and growth

This project allowed me to deepen my experience building interactive data stories entirely with code, combining data analysis in Python with custom front-end visualizations.

Throughout the project, I learned how to:

- Query large public datasets from Base dos Dados using SQL in Python;
- Work with Google BigQuery through the basedosdados package;
- Analyze large datasets using pandas;
- Build interactive visualizations directly in D3.js, including a choropleth map, line chart, sparklines, and waffle charts;
- Create coordinated interactions between multiple visualizations;
- Improve the accessibility of SVG graphics using ARIA attributes and keyboard navigation;

The official documentation for D3 and Base dos Dados, and pandas were my primary references throughout the project. The official documentation for D3, Base dos Dados, and pandas served as my primary references throughout the project. AI-assisted explanations also played an important role in the development process, particularly while building the D3 visualizations, helping me understand unfamiliar concepts, troubleshoot bugs, and experiment with different implementation approaches.

------------------------------------------------------------------------

# Future improvements

Given more time, I would like to:

- Conduct interviews with healthcare professionals, child rights organizations, and girls affected by sexual violence to complement the quantitative analysis;
- Expand the analysis with additional demographic and geographic indicators;
- Continue improving the accessibility of the visualizations, particularly for screen readers;
Refine the mobile experience with layouts specifically designed for smaller screens;
- Add more interactive elements and richer transitions between the visualizations;
- Update the analysis with 2025 data.

------------------------------------------------------------------------

# Tools

- Python
- SQL
- Google BigQuery
- Base dos Dados
- Pandas
- D3.js
- HTML
- CSS
- JavaScript

------------------------------------------------------------------------

# Sources

- Base dos Dados
- Brazilian Ministry of Health (for SINASC data)
- IBGE (for the GeoJSON file)