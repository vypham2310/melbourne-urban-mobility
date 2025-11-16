# Urban Mobility Analysis and Pedestrian Monitoring in Melbourne

This project analyses pedestrian movements across Melbourne CBD using real-time data ingestion, transformation, and visualisation. The solution leverages Azure Data Factory, Azure SQL, and Power BI to ingest, process, and visualise pedestrian traffic patterns for urban planning and policy design.

##  Project Summary

- **Goal**: To identify temporal, spatial, and directional trends in Melbourne’s pedestrian movement, supporting smarter urban mobility planning.
- **Data Sources**:
  - Live pedestrian counts from Melbourne Open Data Platform
  - Sensor metadata (locations and attributes)
- **Tools**:
  - Azure Data Factory
  - Mapping Data Flows
  - Azure Blob Storage
  - Azure SQL Database
  - Power BI

##  Architecture Overview

### 1. Data Ingestion Pipeline
A real-time ingestion pipeline implemented in Azure Data Factory:
- Two Copy Data activities
- Triggers every 15 minutes (`Trigger_15min`)
- Data stored in Azure Blob Storage as raw inputs

### 2. Data Transformation (Mapping Data Flows)
- Merging pedestrian and sensor metadata
- Data cleansing (nulls, negative counts)
- Creating derived attributes (hour, date)
- Aggregation by hour and direction
- Writing transformed data to Azure SQL

### 3. Power BI Dashboard
Provides insights into:
- Hourly and daily pedestrian trends
- Spatial pedestrian load across CBD
- Directional in/out flow analysis
> [View the dashboard here](<https://drive.google.com/file/d/1fmgGWqjo5aphAFJTgTlMfFDzk3bbID46/view?usp=sharing>)

##  Key Insights

### Hourly Movement Pattern
- Two daily peaks: 7 AM and 10 PM
- Lull between 1 PM and 7 PM, ideal for maintenance and upgrades

### Day-of-Week Variance
- Mondays have subdued activity, with movement peaking post 7 PM
- Tuesdays show typical commuter activity: sustained day-long movement

### Spatial Hotspots
- Most traffic occurs along key CBD corridors
- Notable hotspots: State Library precinct, William St – Little Lonsdale St, Flinders St Station underpass

### Directional Flow
- Morning inbound dominance
- Evening outbound flow from CBD

## Urban Planning Recommendations

- Time-aware footpath and lighting improved during peak windows
- Dynamic signage and flow prioritisation during direction-heavy periods
- Enhanced footpath space in high-traffic areas
- Improved shelter and seating at educational and civic hotspots

## Repository Contents
- `pipeline/` Azure Data Factory JSON definitions
- `dataflow/` Mapping Data Flow code
- `visuals/` Power BI dashboard screenshots
- `analysis/` Jupyter or SQL analysis (if applicable)

## Skills Demonstrated
- Real-time data engineering
- Azure cloud services
- ETL pipeline design
- Visual analytics and urban intelligence
- Data-driven recommendations
