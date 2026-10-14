# Skill: ESG Data Audit & Missing Value Detection

## Objective
Analyze the .csv or .xlsx dataset to identify data quality issues, calculate total carbon footprints, and flag missing information.

## Instructions
1. **Load Data**: Ingest the CSV dataset containing employee travel and ESG compliance data.
2. **Missing Data Detection**: 
   - Scan all columns for null, blank, or "Unknown" values.
   - Specifically check `Distance_km` and `Estimated_CO2e_kg`. If distance is missing but CO2 is present (or vice versa), flag as "Partial Data".
3. **Data Validation**:
   - Ensure `Travel_Mode` matches the data (e.g., `Travel_Mode` = "None" must have `Distance_km` = 0).
   - Flag any negative values in distance or emissions.
4. **Aggregation**:
   - Calculate total estimated CO2e for the company.
   - Calculate average CO2e per employee (excluding those with "None" travel).

## Expected Output Format
Provide a structured "Data Audit Summary" containing:
- **Total Records Analyzed**: [Number]
- **Missing Data Flags**: List of Employee IDs and the specific fields missing data.
- **Data Inconsistencies**: List of logical errors (e.g., Flight with 0 distance).
- **Total Carbon Footprint**: [Total CO2e in kg]
