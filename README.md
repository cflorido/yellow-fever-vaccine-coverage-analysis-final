# Yellow Fever Vaccination Analysis - Colombia (2016-2019)

This repository analyzes Yellow Fever vaccination coverage in Colombia between 2016 and 2019 using a Business Intelligence workflow (profiling, ETL, modeling, and dashboarding).

## Main Question
How did Yellow Fever vaccination coverage vary across Colombian regions and departments from 2016 to 2019?

## Project Objectives
- Determine whether there were significant variations in vaccination coverage over time.
- Identify departments and regions with the lowest coverage.
- Contrast coverage behavior against reported mortality patterns.

## Repository Structure
The project has been reorganized to follow a cleaner and more maintainable layout:

```text
yellow-fever-vaccine-coverage-analysis-final/
├─ data/
│  └─ raw/
│     ├─ [IN]Cobertura_Vacunacion_Departamental_2016-2019.xlsx
│     ├─ MuertesFiebreAmarilla.xlsx
│     ├─ Totales.xlsx
│     └─ G19.TemasAnaliticosyDiseñoETL.xlsx
├─ etl/
│  └─ jobProyFinal_ETL.json
├─ notebooks/
│  ├─ analysis/
│  │  └─ FiebreAmarillaPerfilamientoDatos.ipynb
│  └─ profiling/
│     └─ profiling_reports.ipynb
├─ reports/
│  ├─ powerbi/
│  │  └─ ProyectoFinalBI.pbix
│  ├─ presentations/
│  │  └─ PresentacionFinal - Proyecto 2 - BI.pdf
│  └─ diagrams/
│     └─ DiagramaEstrella - Proyecto 2.pdf
└─ README.md
```

## Data and Artifacts
- Raw input datasets: `data/raw/`
- ETL job definition (Glue export): `etl/jobProyFinal_ETL.json`
- Exploratory and analytical notebooks: `notebooks/`
- Final BI deliverables: `reports/`

## Methodology Summary
1. Data ingestion from departmental vaccination coverage and mortality files.
2. Data profiling and cleaning in Python notebooks.
3. ETL pipeline design and cloud data flow (AWS S3 + Glue + Redshift).
4. Star-schema-oriented analytics for reporting.
5. Interactive dashboard delivery in Power BI.

## Key Findings
- Coverage generally improved across years, but territorial disparities remained.
- Some departments (e.g., Vaupes and Guainia) showed high volatility.
- Coverage values above 100% can appear due to migration/floating population effects.
- Mortality concentration is associated with low or inconsistent vaccination coverage zones.

## Power BI Visualizations
<img width="584" height="328" alt="Captura de pantalla 2025-09-21 131547" src="https://github.com/user-attachments/assets/01856735-1883-4ed2-ae37-75646ce35615" />
<img width="583" height="331" alt="Captura de pantalla 2025-09-21 131533" src="https://github.com/user-attachments/assets/e670f360-a9d3-4327-993b-5dfb780a2a48" />
<img width="590" height="331" alt="Captura de pantalla 2025-09-21 131602" src="https://github.com/user-attachments/assets/4baae747-3d80-4dec-84e4-2d6552b4b8d1" />

## Documents
- [Project Report - English](https://github.com/user-attachments/files/22453594/G19.DocumentoProyecto2.1.pdf)
- [Reporte del Proyecto - Espanol](https://github.com/user-attachments/files/22453592/G19.DocumentoProyecto2.pdf)

## Presentations
- [Presentation - English](https://github.com/user-attachments/files/22453598/PresentacionFinal.-.Proyecto.2.-.BI.pdf)
- [Presentacion - Espanol](https://github.com/user-attachments/files/22453591/PresentacionFinal.-.Proyecto.2.-.BI.pdf)

## Authors
- Sarah Theresa Monroe Aranzazu - 202211145 (MED)
- Natalia Villegas Calderon - 202113370 (ING)
- Juan Martin Vasquez Cristancho - 202113314 (IN)
- Carol Sofia Florido Castro - 202111430 (ING)

Courses:
- Business Intelligence - ISIS 3301
- Clinical Decision Elements II - MEDI-2109

University: Universidad de los Andes - Bogota, Colombia
Year: 2025

## Technologies
- Python 3.11
- AWS S3, AWS Glue, AWS Redshift
- Power BI
- pandas, numpy, matplotlib, seaborn
- ydata_profiling
- scikit-learn
- SQL

