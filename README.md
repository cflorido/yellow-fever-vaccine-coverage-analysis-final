# Yellow Fever Vaccination Analysis – Colombia (2016–2019)

This project focuses on analyzing vaccination rates against **Yellow Fever** in Colombia between 2016 and 2019. Yellow Fever is a viral disease transmitted by mosquitoes and preventable with a single dose of vaccine, which provides lifetime protection. Despite Colombia’s national vaccination program (PAI), outbreaks and fatalities still occur, highlighting the need for improved strategies.  

The main research question addressed is:  
**How do Yellow Fever vaccination rates vary in Colombia between 2016 and 2019?**

The project applies a **Business Intelligence approach** by integrating epidemiological data, building data marts, applying descriptive and inferential analysis, and visualizing results in interactive dashboards. The outcomes aim to support the Colombian Ministry of Health in reinforcing strategies, allocating resources, and improving vaccination coverage in vulnerable regions.  

---

## Project Objectives
- **Main Objective**  
  - Determine whether there were variations in Yellow Fever vaccination rates in Colombia between 2016 and 2019.  

- **Secondary Objectives**  
  - Identify the region with the lowest vaccination rate.  
  - Identify the department with the lowest vaccination rate.  
  - Analyze the vaccination rate incidence across Colombia’s six regions.  

---

## Methodology
1. **Data Understanding**  
   - Data source: `Cobertura_Vacunacion_Departamental_2016-2019.xlsx` (coverage by year and department).  
   - Integrated with mortality data from the **Instituto Nacional de Salud (INS)** (2016–2019).  
   - Key variables: population at 1 year, doses administered, coverage %, and reported deaths.  

2. **ETL Architecture (AWS-based)**  
   - **Extract**: Raw Excel datasets and INS reports.  
   - **Transform**: Preprocessing and cleaning performed with **Python**.  
   - **Load**:  
     - Data stored in **AWS S3**.  
     - ETL executed with **AWS Glue**.  
     - Data loaded into **AWS Redshift**, structured in a **star schema** (fact and dimension tables).  

3. **Data Profiling & Quality**  
   - No missing or duplicate records.  
   - Coverage values sometimes exceeded 100% (due to migration, floating population, or population underestimation).  
   - Variations detected across regions, with some departments below the 95% coverage goal.  

4. **Visualization**  
   - Interactive dashboards developed in **Power BI**, connected to AWS Redshift.  
   - Provided multidimensional analysis by year, region, and department.  

---

## Key Findings
- Coverage generally improved from 2016 to 2019, but disparities persisted between departments.  
- Departments like **Vaupés and Guainía** showed strong fluctuations in vaccination coverage.  
- Some regions exceeded 100% coverage due to vaccination of non-resident or migrant populations.  
- Most Yellow Fever deaths occurred in areas with **low or inconsistent vaccination coverage**, highlighting public health risks.  

---

## Documents
- [Project Report – English](https://github.com/user-attachments/files/22453594/G19.DocumentoProyecto2.1.pdf)
- [Reporte del Proyecto – Español](https://github.com/user-attachments/files/22453592/G19.DocumentoProyecto2.pdf)


---
## Presentations
- [Presentation – English](https://github.com/user-attachments/files/22453598/PresentacionFinal.-.Proyecto.2.-.BI.pdf)

- [Presentación – Español](https://github.com/user-attachments/files/22453591/PresentacionFinal.-.Proyecto.2.-.BI.pdf)

---

## Authors
- Sarah Theresa Monroe Aranzazu – 202211145 (MED)  
- Natalia Villegas Calderón – 202113370 (ING)  
- Juan Martín Vásquez Cristancho – 202113314 (IN)  
- Carol Sofía Florido Castro – 202111430 (ING)  

Courses:  
- Business Intelligence – ISIS 3301  
- Clinical Decision Elements II – MEDI-2109  
University: **Universidad de los Andes – Bogotá, Colombia**  
Year: **2025**  

---

## Technologies Used

- Python 3.11
- AWS S3 (data storage)
- AWS Glue (ETL orchestration)
- AWS Redshift (data warehouse, star schema)
- Power BI (interactive dashboards)
- pandas, numpy, matplotlib, seaborn
- ydata_profiling (data profiling)
- scikit-learn (statistical tests, ANOVA)
- SQL (Data Mart design)

