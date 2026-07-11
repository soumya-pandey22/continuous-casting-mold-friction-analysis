# Continuous Casting Mold Friction Calculation from the Available Hydraulic Force Data 🏭

## Overview
This project focuses on the calculation of mold friction 
in continuous casting using available hydraulic force data,
conducted during Vocational Training at Tata Steel R&D, 
Jamshedpur.

Mold friction is a critical parameter that directly affects 
the surface quality and defect formation in continuously 
cast steel. This project applies the Force Difference Method 
(MDF) to calculate mold friction from hydraulic force data.

## Objectives
- Calculate mold friction using hydraulic force data
- Apply the Force Difference Method (MDF)
- Analyze Hot Run and Cold Run force patterns
- Understand Positive and Negative Strip Time behavior
- Plot and compare MDF, Hot Run and Cold Run force graphs
- Validate results against published literature data
- (Upcoming) Analyze using actual plant data from Tata Steel

## Theory

### Force Balance Equations

**Cold Run (without steel):**
F(t)Cold = F(t)Inertia + F(t)Weight + F(t)Mechanical
Where:
- F(t)Inertia = Force due to acceleration of oscillating mold mass
- F(t)Weight = Weight of oscillating mold assembly
- F(t)Mechanical = Losses inside oscillating equipment (bearing loss etc.)

**Hot Run (with steel):**
F(t)Hot = F(t)Inertia + F(t)Weight + F(t)Mechanical + F(t)Friction
Where:
- F(t)Friction = Mold friction force (MDF)

### Force Difference Method (MDF)
MDF is calculated as the difference between Hot Run 
and Cold Run forces:
MDF = F(t)Hot - F(t)Cold = F(t)Friction

### Strip Time Analysis
**Positive Strip Time:**
Duration during which mold velocity is lower than casting 
speed, or mold moves upward. During this period:
- Strand moves downward faster relative to mold
- Upward frictional force acts on mold
- Tensile stresses increase in solidifying shell

**Negative Strip Time:**
Duration during which mold moves downward faster than 
casting speed. During this period:
- Friction force direction reverses
- Downward frictional force acts on mold
- Reduces tensile stress in shell
- Helps close surface cracks
- Promotes liquid mold flux infiltration
- Improves lubrication between mold and solidifying shell

The balance between positive and negative strip time plays 
a critical role in controlling mold friction, lubrication 
behaviour, and surface quality of continuously cast products.

## Data Extraction using PlotDigitizer
Since the original force vs time graphs from research 
literature did not provide numerical values at small time 
intervals, PlotDigitizer was used to extract precise 
data points from the graph images.

- Source: Published research paper on continuous casting
- Tool: PlotDigitizer PRO
- Data extracted: Hot Run and Cold Run force values 
  at small time intervals
- Data points extracted: ~10 points (can be increased 
  for higher resolution analysis)
- Extracted data was stored in Excel/CSV format for 
  further processing in Python

## Key Observations from Graphs
- Hot Run force shows highest peak as it contains all Cold 
  Run force terms plus additional friction force term
- Cold Run force has lower peak as it excludes friction force
- Positive MDF indicates upward friction direction
- Negative MDF indicates downward friction direction
- MDF sign change represents transition between positive 
  and negative strip time

## Methodology
1. Identified relevant force vs time graphs from 
   research literature
2. Extracted Hot Run and Cold Run force data points 
   using PlotDigitizer at small time intervals
3. Stored and organized extracted data in Excel/CSV format
4. Wrote Python code to calculate MDF values
5. Generated graphs using Matplotlib for analysis
6. Analyzed strip time behavior from MDF graphs

## Dataset
- Source: Literature data (Phase 1)
- Upcoming: Plant data from Tata Steel SMS/IBA system
- Parameters: Hot Run Force, Cold Run Force, Time

## Tools Used
- Python (Jupyter Notebook)
- Pandas, Matplotlib, Numpy, Scipy
- Microsoft Excel
- PlotDigitizer PRO

## Current Status
✅ Phase 1: Literature data analysis complete  
🔜 Phase 2: Plant data analysis in progress

## Skills Demonstrated
- Manufacturing Research
- Continuous Casting Process Knowledge
- Hydraulic Force Data Analysis
- Data Extraction from Research Literature
- Strip Time Analysis
- Python Programming
- Data Visualization
